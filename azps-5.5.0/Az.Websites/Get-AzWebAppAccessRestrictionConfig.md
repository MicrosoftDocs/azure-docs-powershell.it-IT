---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182463"
---
# <span data-ttu-id="42760-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="42760-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="42760-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42760-102">SYNOPSIS</span></span>
<span data-ttu-id="42760-103">Recupera la configurazione di ritienizione di Access per un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="42760-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="42760-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42760-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42760-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="42760-105">DESCRIPTION</span></span>
<span data-ttu-id="42760-106">Il cmdlet **Get-AzWebAppAccessRestrictionConfig** ottiene la configurazione di Restrizione di accesso per un'app Web di Azure.</span><span class="sxs-lookup"><span data-stu-id="42760-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="42760-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42760-107">EXAMPLES</span></span>

### <span data-ttu-id="42760-108">Esempio 1: Ottenere una configurazione delle restrizioni di accesso all'app Web da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="42760-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="42760-109">Questo comando recupera la configurazione delle restrizioni di accesso di un'app Web denominata ContosoSite che appartiene al gruppo di risorse Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="42760-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="42760-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42760-110">PARAMETERS</span></span>

### <span data-ttu-id="42760-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42760-111">-DefaultProfile</span></span>
<span data-ttu-id="42760-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42760-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42760-113">-Name</span><span class="sxs-lookup"><span data-stu-id="42760-113">-Name</span></span>
<span data-ttu-id="42760-114">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="42760-114">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42760-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42760-115">-ResourceGroupName</span></span>
<span data-ttu-id="42760-116">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="42760-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42760-117">-SlotName</span><span class="sxs-lookup"><span data-stu-id="42760-117">-SlotName</span></span>
<span data-ttu-id="42760-118">Nome slot di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="42760-118">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42760-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42760-119">CommonParameters</span></span>
<span data-ttu-id="42760-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42760-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42760-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="42760-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42760-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="42760-122">INPUTS</span></span>

### <span data-ttu-id="42760-123">System.String</span><span class="sxs-lookup"><span data-stu-id="42760-123">System.String</span></span>

## <span data-ttu-id="42760-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42760-124">OUTPUTS</span></span>

### <span data-ttu-id="42760-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="42760-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="42760-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="42760-126">NOTES</span></span>

## <span data-ttu-id="42760-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42760-127">RELATED LINKS</span></span>

[<span data-ttu-id="42760-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="42760-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="42760-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="42760-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="42760-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="42760-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
