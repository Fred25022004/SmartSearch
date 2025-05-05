# SmartSearch
An AI-Enhanced Multi-Modal Search Engine for Medical Content

Initial Notes for Developers: 

# 开发分支
每次新功能（如“多模态编码器集成”）先新建分支：
git checkout -b feature/multimodal-encoder

# 编写代码
在 smartsearch/multimodal/ 下引入 external/med3dvlm 的 DCFormer、SigLIP；
在 smartsearch/retrieval/ 编写与 FAISS 或 Qdrant 交互的向量检索模块；
在 backend/app/routers/query.py 实现新的查询 API；
在 frontend/src/pages/ 下编写对应的页面，调用后端接口。

# 测试与提交
pytest tests/        # 运行后端测试
cd frontend && npm test   # 运行前端测试
git add .
git commit -m "Integrate Med3DVLM encoder and retrieval module"
git push origin feature/multimodal-encoder

# Pull Request
在 GitHub 上为 feature/* 分支发起 PR，让团队成员 Review、合并到 master。


