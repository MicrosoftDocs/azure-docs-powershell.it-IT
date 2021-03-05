---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: d351ab76941d16e3d3e091e223524863d4256d75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986591"
---
# <span data-ttu-id="0f71f-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="0f71f-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="0f71f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f71f-102">SYNOPSIS</span></span>
<span data-ttu-id="0f71f-103">Ottiene le soluzioni di sicurezza individuate dal Centro sicurezza di Azure</span><span class="sxs-lookup"><span data-stu-id="0f71f-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="0f71f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f71f-104">SYNTAX</span></span>

### <span data-ttu-id="0f71f-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f71f-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f71f-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="0f71f-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f71f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f71f-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f71f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0f71f-108">DESCRIPTION</span></span>
<span data-ttu-id="0f71f-109">Le soluzioni di sicurezza vengono individuate automaticamente dal Centro sicurezza di Azure. Usare questo cmdlet per visualizzare le soluzioni di sicurezza individuate</span><span class="sxs-lookup"><span data-stu-id="0f71f-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="0f71f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f71f-110">EXAMPLES</span></span>

### <span data-ttu-id="0f71f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0f71f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="0f71f-112">Ottenere tutte le soluzioni di sicurezza individuate nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="0f71f-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="0f71f-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0f71f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="0f71f-114">Ottenere una specifica soluzione di sicurezza individuata</span><span class="sxs-lookup"><span data-stu-id="0f71f-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="0f71f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f71f-115">PARAMETERS</span></span>

### <span data-ttu-id="0f71f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f71f-116">-DefaultProfile</span></span>
<span data-ttu-id="0f71f-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f71f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f71f-118">-Location</span><span class="sxs-lookup"><span data-stu-id="0f71f-118">-Location</span></span>
<span data-ttu-id="0f71f-119">Posizione.</span><span class="sxs-lookup"><span data-stu-id="0f71f-119">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f71f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0f71f-120">-Name</span></span>
<span data-ttu-id="0f71f-121">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f71f-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f71f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f71f-122">-ResourceGroupName</span></span>
<span data-ttu-id="0f71f-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0f71f-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f71f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f71f-124">-ResourceId</span></span>
<span data-ttu-id="0f71f-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f71f-125">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f71f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f71f-126">CommonParameters</span></span>
<span data-ttu-id="0f71f-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f71f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f71f-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0f71f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f71f-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="0f71f-129">INPUTS</span></span>

### <span data-ttu-id="0f71f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0f71f-130">System.String</span></span>

## <span data-ttu-id="0f71f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f71f-131">OUTPUTS</span></span>

### <span data-ttu-id="0f71f-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="0f71f-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="0f71f-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="0f71f-133">NOTES</span></span>

## <span data-ttu-id="0f71f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f71f-134">RELATED LINKS</span></span>
