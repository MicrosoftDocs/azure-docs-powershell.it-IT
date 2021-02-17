---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 2b49b30c06f39561f6d00542dd4ff02df56ee569
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198206"
---
# <span data-ttu-id="5e314-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="5e314-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="5e314-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e314-102">SYNOPSIS</span></span>
<span data-ttu-id="5e314-103">Get-AzWebAppContainerContinuousDeploymentUrl restituirà l'URL di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="5e314-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="5e314-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e314-104">SYNTAX</span></span>

### <span data-ttu-id="5e314-105">S1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e314-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e314-106">S2</span><span class="sxs-lookup"><span data-stu-id="5e314-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e314-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5e314-107">DESCRIPTION</span></span>
<span data-ttu-id="5e314-108">Get-AzWebAppContainerContinuousDeploymentUrl restituirà l'URL di distribuzione continua del contenitore</span><span class="sxs-lookup"><span data-stu-id="5e314-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="5e314-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e314-109">EXAMPLES</span></span>

### <span data-ttu-id="5e314-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5e314-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="5e314-111">Questo comando restituirà l'URL di distribuzione continua del contenitore.</span><span class="sxs-lookup"><span data-stu-id="5e314-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="5e314-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e314-112">PARAMETERS</span></span>

### <span data-ttu-id="5e314-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e314-113">-DefaultProfile</span></span>
<span data-ttu-id="5e314-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e314-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e314-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5e314-115">-Name</span></span>
<span data-ttu-id="5e314-116">Il nome dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="5e314-116">The name of the web app.</span></span>

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

### <span data-ttu-id="5e314-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e314-117">-ResourceGroupName</span></span>
<span data-ttu-id="5e314-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5e314-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="5e314-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="5e314-119">-SlotName</span></span>
<span data-ttu-id="5e314-120">Nome dello slot dell'app Web.</span><span class="sxs-lookup"><span data-stu-id="5e314-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="5e314-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5e314-121">-WebApp</span></span>
<span data-ttu-id="5e314-122">Oggetto app Web</span><span class="sxs-lookup"><span data-stu-id="5e314-122">The web app object</span></span>

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

### <span data-ttu-id="5e314-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e314-123">CommonParameters</span></span>
<span data-ttu-id="5e314-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e314-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e314-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e314-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e314-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="5e314-126">INPUTS</span></span>

### <span data-ttu-id="5e314-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5e314-127">System.String</span></span>

### <span data-ttu-id="5e314-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="5e314-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5e314-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e314-129">OUTPUTS</span></span>

### <span data-ttu-id="5e314-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5e314-130">System.String</span></span>

## <span data-ttu-id="5e314-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="5e314-131">NOTES</span></span>

## <span data-ttu-id="5e314-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e314-132">RELATED LINKS</span></span>
