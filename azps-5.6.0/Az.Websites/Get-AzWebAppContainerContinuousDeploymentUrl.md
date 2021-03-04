---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 90aca2939721144500519329492e04786b67a93a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981757"
---
# <span data-ttu-id="99e45-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="99e45-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="99e45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99e45-102">SYNOPSIS</span></span>
<span data-ttu-id="99e45-103">Get-AzWebAppContainerContinuousDeploymentUrl restituirà l'URL di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="99e45-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="99e45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99e45-104">SYNTAX</span></span>

### <span data-ttu-id="99e45-105">S1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99e45-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99e45-106">S2</span><span class="sxs-lookup"><span data-stu-id="99e45-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99e45-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="99e45-107">DESCRIPTION</span></span>
<span data-ttu-id="99e45-108">Get-AzWebAppContainerContinuousDeploymentUrl restituirà l'URL di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="99e45-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="99e45-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99e45-109">EXAMPLES</span></span>

### <span data-ttu-id="99e45-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99e45-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="99e45-111">Questo comando restituirà l'URL di distribuzione continua del contenitore.</span><span class="sxs-lookup"><span data-stu-id="99e45-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="99e45-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99e45-112">PARAMETERS</span></span>

### <span data-ttu-id="99e45-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e45-113">-DefaultProfile</span></span>
<span data-ttu-id="99e45-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99e45-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99e45-115">-Name</span><span class="sxs-lookup"><span data-stu-id="99e45-115">-Name</span></span>
<span data-ttu-id="99e45-116">Nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="99e45-116">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e45-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99e45-117">-ResourceGroupName</span></span>
<span data-ttu-id="99e45-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="99e45-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99e45-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="99e45-119">-SlotName</span></span>
<span data-ttu-id="99e45-120">Nome dello slot dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="99e45-120">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99e45-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="99e45-121">-WebApp</span></span>
<span data-ttu-id="99e45-122">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="99e45-122">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99e45-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e45-123">CommonParameters</span></span>
<span data-ttu-id="99e45-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99e45-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e45-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99e45-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e45-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="99e45-126">INPUTS</span></span>

### <span data-ttu-id="99e45-127">System.String</span><span class="sxs-lookup"><span data-stu-id="99e45-127">System.String</span></span>

### <span data-ttu-id="99e45-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="99e45-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="99e45-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99e45-129">OUTPUTS</span></span>

### <span data-ttu-id="99e45-130">System.String</span><span class="sxs-lookup"><span data-stu-id="99e45-130">System.String</span></span>

## <span data-ttu-id="99e45-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="99e45-131">NOTES</span></span>

## <span data-ttu-id="99e45-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99e45-132">RELATED LINKS</span></span>
