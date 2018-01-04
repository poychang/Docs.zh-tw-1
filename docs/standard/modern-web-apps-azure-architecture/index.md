---
title: "使用 ASP.NET Core 和 Azure 架構現代化 Web 應用程式"
description: "使用 ASP.NET Core 和 Azure 架構現代化 Web 應用程式 | 簡介"
author: ardalis
ms.author: wiwagn
ms.date: 10/06/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 44864274a86634c0199885b5507124f2f54ce0f6
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/23/2017
---
# <a name="architect-modern-web-applications-with-aspnet-core-and-azure"></a><span data-ttu-id="1635e-103">使用 ASP.NET Core 和 Azure 架構現代化 Web 應用程式</span><span class="sxs-lookup"><span data-stu-id="1635e-103">Architect Modern Web Applications with ASP.NET Core and Azure</span></span>

<span data-ttu-id="1635e-104">.NET Core 和 ASP.NET Core 提供許多優於傳統.NET 開發的優點。</span><span class="sxs-lookup"><span data-stu-id="1635e-104">.NET Core and ASP.NET Core offer several advantages over traditional .NET development.</span></span> <span data-ttu-id="1635e-105">如果下列部分或所有項目對應用程式成功而言十分重要，則您應該將 .NET Core 用於伺服器應用程式：</span><span class="sxs-lookup"><span data-stu-id="1635e-105">You should use .NET Core for your server applications if some or all of the following are important to your application's success:</span></span>

-   <span data-ttu-id="1635e-106">跨平台支援</span><span class="sxs-lookup"><span data-stu-id="1635e-106">Cross-platform support</span></span>

-   <span data-ttu-id="1635e-107">使用微服務</span><span class="sxs-lookup"><span data-stu-id="1635e-107">Use of microservices</span></span>

-   <span data-ttu-id="1635e-108">使用 Docker 容器</span><span class="sxs-lookup"><span data-stu-id="1635e-108">Use of Docker containers</span></span>

-   <span data-ttu-id="1635e-109">高效能和延展性需求</span><span class="sxs-lookup"><span data-stu-id="1635e-109">High performance and scalability requirements</span></span>

-   <span data-ttu-id="1635e-110">相同伺服器上應用程式之 .NET 版本的並存版本控制</span><span class="sxs-lookup"><span data-stu-id="1635e-110">Side-by-side versioning of .NET versions by application on the same server</span></span>

<span data-ttu-id="1635e-111">傳統 .NET 應用程式可以並確實支援這些需求，但 ASP.NET Core 和 .NET Core 已最佳化可提供針對上述案例的改善支援。</span><span class="sxs-lookup"><span data-stu-id="1635e-111">Traditional .NET applications can and do support these requirements, but ASP.NET Core and .NET Core have been optimized to offer improved support for the above scenarios.</span></span>

<span data-ttu-id="1635e-112">越來越多的組織會選擇使用 Microsoft Azure 這類服務，以在雲端中裝載其 Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="1635e-112">More and more organizations are choosing to host their web applications in the cloud using services like Microsoft Azure.</span></span> <span data-ttu-id="1635e-113">如果下列對您的應用程式或組織十分重要，則您應該考慮將應用程式裝載在雲端中：</span><span class="sxs-lookup"><span data-stu-id="1635e-113">You should consider hosting your application in the cloud if the following are important to your application or organization:</span></span>

-   <span data-ttu-id="1635e-114">降低對資料中心成本的投資 (硬體、軟體、空間、公用程式等等)</span><span class="sxs-lookup"><span data-stu-id="1635e-114">Reduced investment in data center costs (hardware, software, space, utilities, etc)</span></span>

-   <span data-ttu-id="1635e-115">彈性價格 (根據使用付費，而閒置容量不需付費)</span><span class="sxs-lookup"><span data-stu-id="1635e-115">Flexible pricing (pay based on usage, not for idle capacity)</span></span>

-   <span data-ttu-id="1635e-116">極高可靠性</span><span class="sxs-lookup"><span data-stu-id="1635e-116">Extreme reliability</span></span>

-   <span data-ttu-id="1635e-117">改善的應用程式行動性；輕鬆地變更您應用程式的部署位置和方式</span><span class="sxs-lookup"><span data-stu-id="1635e-117">Improved app mobility; easily change where and how your app is deployed</span></span>

-   <span data-ttu-id="1635e-118">彈性容量；根據實際需求相應增加或減少</span><span class="sxs-lookup"><span data-stu-id="1635e-118">Flexible capacity; scale up or down based on actual needs</span></span>

<span data-ttu-id="1635e-119">使用 ASP.NET Core 建置 Web 應用程式 (且其裝載於 Microsoft Azure) 提供許多優於傳統替代項目的具競爭性優點。</span><span class="sxs-lookup"><span data-stu-id="1635e-119">Building web applications with ASP.NET Core, hosted in Microsoft Azure, offers numerous competitive advantages over traditional alternatives.</span></span> <span data-ttu-id="1635e-120">ASP.NET Core 已針對現代化 Web 應用程式開發做法和雲端裝載案例最佳化。</span><span class="sxs-lookup"><span data-stu-id="1635e-120">ASP.NET Core is optimized for modern web application development practices and cloud hosting scenarios.</span></span> <span data-ttu-id="1635e-121">在本指南中，您將學習如何架構 ASP.NET Core 應用程式以善加利用這些功能。</span><span class="sxs-lookup"><span data-stu-id="1635e-121">In this guide, you will learn how to architect your ASP.NET Core applications to best take advantage of these capabilities.</span></span>

## <a name="purpose"></a><span data-ttu-id="1635e-122">用途</span><span class="sxs-lookup"><span data-stu-id="1635e-122">Purpose</span></span>

<span data-ttu-id="1635e-123">本指南會提供使用 ASP.NET Core 和 Azure 建置整合型 Web 應用程式的端對端指引。</span><span class="sxs-lookup"><span data-stu-id="1635e-123">This guide provides end-to-end guidance on building monolithic web applications using ASP.NET Core and Azure.</span></span>

<span data-ttu-id="1635e-124">本指南可補充「使用 .NET 架構和開發容器化和以微服務為基礎的應用程式」，其較著重 Docker、微服務以及裝載企業應用程式的容器的部署。</span><span class="sxs-lookup"><span data-stu-id="1635e-124">This guide is complementary to the "*Architecting and Developing Containerized and Microservice-based Applications with .NET*" which focuses more on Docker, Microservices, and Deployment of Containers to host enterprise applications.</span></span>

> ### <a name="architecting-and-developing-containerized-microservice-based-apps-in-net"></a><span data-ttu-id="1635e-125">在 .NET 中架構和開發以容器化微服務為基礎的應用程式</span><span class="sxs-lookup"><span data-stu-id="1635e-125">Architecting and Developing Containerized Microservice Based Apps in .NET</span></span>
> - <span data-ttu-id="1635e-126">**電子書**</span><span class="sxs-lookup"><span data-stu-id="1635e-126">**e-book**</span></span>  
> <span data-ttu-id="1635e-127"><http://aka.ms/MicroservicesEbook></span><span class="sxs-lookup"><span data-stu-id="1635e-127"><http://aka.ms/MicroservicesEbook></span></span>
> - <span data-ttu-id="1635e-128">**範例應用程式**</span><span class="sxs-lookup"><span data-stu-id="1635e-128">**Sample Application**</span></span>  
> <span data-ttu-id="1635e-129"><http://aka.ms/microservicesarchitecture></span><span class="sxs-lookup"><span data-stu-id="1635e-129"><http://aka.ms/microservicesarchitecture></span></span>

## <a name="who-should-use-this-guide"></a><span data-ttu-id="1635e-130">誰應該使用本指南</span><span class="sxs-lookup"><span data-stu-id="1635e-130">Who should use this guide</span></span>

<span data-ttu-id="1635e-131">本指南的對象主要是開發人員、開發負責人和架構設計人員，而他們對使用 Microsoft 技術和服務在雲端中建置現代化 Web 應用程式感興趣。</span><span class="sxs-lookup"><span data-stu-id="1635e-131">The audience for this guide is mainly developers, development leads, and architects who are interested in building modern web applications using Microsoft technologies and services in the cloud.</span></span>

<span data-ttu-id="1635e-132">次要對象是技術決策者，其已熟悉 ASP.NET 和 (或) Azure，並尋找是否可以升級為新或現有專案之 ASP.NET Core 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1635e-132">A secondary audience is technical decision makers who are already familiar ASP.NET and/or Azure and are looking for information on whether it makes sense to upgrade to ASP.NET Core for new or existing projects.</span></span>

## <a name="how-you-can-use-this-guide"></a><span data-ttu-id="1635e-133">此指南的使用方式</span><span class="sxs-lookup"><span data-stu-id="1635e-133">How you can use this guide</span></span>

<span data-ttu-id="1635e-134">本指南已壓縮成相當小的文件，著重於使用現代化 .NET 技術和 Windows Azure 來建置 Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="1635e-134">This guide has been condensed into a relatively small document that focuses on building web applications with modern .NET technologies and Windows Azure.</span></span> <span data-ttu-id="1635e-135">因此，可以完整讀取它，以提供對這類應用程式和其技術考量的基礎了解。</span><span class="sxs-lookup"><span data-stu-id="1635e-135">As such, it can be read in its entirety to provide a foundation of understanding such applications and their technical considerations.</span></span> <span data-ttu-id="1635e-136">本指南與其範例應用程式也可以作為起點或參考。</span><span class="sxs-lookup"><span data-stu-id="1635e-136">The guide, along with its sample application, can also serve as a starting point or reference.</span></span> <span data-ttu-id="1635e-137">使用相關聯的範例應用程式作為您專屬應用程式的範本，或查看如何組織應用程式的元件組件。</span><span class="sxs-lookup"><span data-stu-id="1635e-137">Use the associated sample application as a template for your own applications, or to see how you might organize your application's component parts.</span></span> <span data-ttu-id="1635e-138">請回頭參考指南的原則、架構和技術選項的涵蓋範圍，以及權衡這些針對您專屬應用程式之選擇的決策考量。</span><span class="sxs-lookup"><span data-stu-id="1635e-138">Refer back to the guide's principles and coverage of architecture and technology options and decision considerations when weighing these choices for your own application.</span></span>

<span data-ttu-id="1635e-139">請隨意將本指南轉寄給您的小組，協助確保對這些考量和機會有共同的了解。</span><span class="sxs-lookup"><span data-stu-id="1635e-139">Feel free to forward this guide to your team to help ensure a common understanding of these considerations and opportunities.</span></span> <span data-ttu-id="1635e-140">讓所有人都使用一組共用術語和基礎原則，將有助於確保套用一致的架構模式和做法。</span><span class="sxs-lookup"><span data-stu-id="1635e-140">Having everybody working from a common set of terminology and underlying principles will help ensure consistent application of architectural patterns and practices.</span></span>

## <a name="references"></a><span data-ttu-id="1635e-141">參考</span><span class="sxs-lookup"><span data-stu-id="1635e-141">References</span></span>
- <span data-ttu-id="1635e-142">**針對伺服器應用程式在 .NET Core 和 .NET Framework 之間進行選擇**</span><span class="sxs-lookup"><span data-stu-id="1635e-142">**Choosing between .NET Core and .NET Framework for server apps**</span></span>  
<span data-ttu-id="1635e-143"><https://docs.microsoft.com/dotnet/articles/standard/choosing-core-framework-server></span><span class="sxs-lookup"><span data-stu-id="1635e-143"><https://docs.microsoft.com/dotnet/articles/standard/choosing-core-framework-server></span></span>

>[!div class="step-by-step"]
<span data-ttu-id="1635e-144">[下一個] (modern-web-applications-characteristics.md)</span><span class="sxs-lookup"><span data-stu-id="1635e-144">[Next] (modern-web-applications-characteristics.md)</span></span>