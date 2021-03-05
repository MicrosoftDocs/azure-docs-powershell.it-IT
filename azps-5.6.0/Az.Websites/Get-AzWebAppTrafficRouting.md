---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007422"
---
# <span data-ttu-id="fc832-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="fc832-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="fc832-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc832-102">SYNOPSIS</span></span>
<span data-ttu-id="fc832-103">Ottenere una regola di routing per il nome assegnato dello slot.</span><span class="sxs-lookup"><span data-stu-id="fc832-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="fc832-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc832-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc832-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fc832-105">DESCRIPTION</span></span>
<span data-ttu-id="fc832-106">Il cmdlet **Get-AzWebAppTrafficRouting ottiene** una configurazione della regola di routing da uno slot Di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="fc832-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="fc832-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc832-107">EXAMPLES</span></span>

### <span data-ttu-id="fc832-108">Esempio 1: ottiene la regola di routing specifica dallo slot della webapp</span><span class="sxs-lookup"><span data-stu-id="fc832-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="fc832-109">Questo comando ottiene una regola di routing per un determinato slot webapp.</span><span class="sxs-lookup"><span data-stu-id="fc832-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="fc832-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc832-110">PARAMETERS</span></span>

### <span data-ttu-id="fc832-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc832-111">-DefaultProfile</span></span>
<span data-ttu-id="fc832-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc832-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc832-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc832-113">-ResourceGroupName</span></span>
<span data-ttu-id="fc832-114">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fc832-114">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc832-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="fc832-115">-RuleName</span></span>
<span data-ttu-id="fc832-116">Nome regola</span><span class="sxs-lookup"><span data-stu-id="fc832-116">Rule Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc832-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="fc832-117">-WebAppName</span></span>
<span data-ttu-id="fc832-118">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="fc832-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc832-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc832-119">CommonParameters</span></span>
<span data-ttu-id="fc832-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc832-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc832-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fc832-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc832-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="fc832-122">INPUTS</span></span>

### <span data-ttu-id="fc832-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fc832-123">None</span></span>

## <span data-ttu-id="fc832-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc832-124">OUTPUTS</span></span>

### <span data-ttu-id="fc832-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="fc832-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="fc832-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="fc832-126">NOTES</span></span>

## <span data-ttu-id="fc832-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc832-127">RELATED LINKS</span></span>

[<span data-ttu-id="fc832-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="fc832-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="fc832-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="fc832-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="fc832-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="fc832-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
