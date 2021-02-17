---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198199"
---
# <span data-ttu-id="dee6b-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="dee6b-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="dee6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dee6b-102">SYNOPSIS</span></span>
<span data-ttu-id="dee6b-103">Ottenere una regola di routing per il nome assegnato dello slot.</span><span class="sxs-lookup"><span data-stu-id="dee6b-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="dee6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dee6b-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dee6b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dee6b-105">DESCRIPTION</span></span>
<span data-ttu-id="dee6b-106">Il cmdlet **Get-AzWebAppTrafficRouting ottiene** una configurazione della regola di routing da uno slot Di Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="dee6b-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="dee6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dee6b-107">EXAMPLES</span></span>

### <span data-ttu-id="dee6b-108">Esempio 1: ottiene la regola di routing specifica dallo slot della webapp</span><span class="sxs-lookup"><span data-stu-id="dee6b-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="dee6b-109">Questo comando ottiene una regola di routing per un determinato slot webapp.</span><span class="sxs-lookup"><span data-stu-id="dee6b-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="dee6b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dee6b-110">PARAMETERS</span></span>

### <span data-ttu-id="dee6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee6b-111">-DefaultProfile</span></span>
<span data-ttu-id="dee6b-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dee6b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dee6b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dee6b-113">-ResourceGroupName</span></span>
<span data-ttu-id="dee6b-114">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="dee6b-114">Resource Group Name</span></span>

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

### <span data-ttu-id="dee6b-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="dee6b-115">-RuleName</span></span>
<span data-ttu-id="dee6b-116">Nome regola</span><span class="sxs-lookup"><span data-stu-id="dee6b-116">Rule Name</span></span>
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

### <span data-ttu-id="dee6b-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="dee6b-117">-WebAppName</span></span>
<span data-ttu-id="dee6b-118">Nome WebApp</span><span class="sxs-lookup"><span data-stu-id="dee6b-118">WebApp Name</span></span>

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

### <span data-ttu-id="dee6b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee6b-119">CommonParameters</span></span>
<span data-ttu-id="dee6b-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dee6b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee6b-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dee6b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee6b-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="dee6b-122">INPUTS</span></span>

### <span data-ttu-id="dee6b-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="dee6b-123">None</span></span>

## <span data-ttu-id="dee6b-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dee6b-124">OUTPUTS</span></span>

### <span data-ttu-id="dee6b-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="dee6b-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="dee6b-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="dee6b-126">NOTES</span></span>

## <span data-ttu-id="dee6b-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dee6b-127">RELATED LINKS</span></span>

[<span data-ttu-id="dee6b-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="dee6b-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="dee6b-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="dee6b-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="dee6b-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="dee6b-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
