---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDiscoveredSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDiscoveredSecuritySolution.md
ms.openlocfilehash: e81224796d8f38f15d8c3a08e5b572c8f3aab117
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022644"
---
# <span data-ttu-id="52ca9-101">Get-AzDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="52ca9-101">Get-AzDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="52ca9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="52ca9-103">Ottiene soluzioni di sicurezza individuate da Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="52ca9-103">Gets security solutions that were discovered by Azure Security Center</span></span>

## <span data-ttu-id="52ca9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52ca9-104">SYNTAX</span></span>

### <span data-ttu-id="52ca9-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="52ca9-105">SubscriptionScope (Default)</span></span>
```
Get-AzDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52ca9-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="52ca9-106">ResourceGroupLevelResource</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52ca9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="52ca9-107">ResourceId</span></span>
```
Get-AzDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52ca9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52ca9-108">DESCRIPTION</span></span>
<span data-ttu-id="52ca9-109">Le soluzioni di sicurezza vengono scoperte automaticamente da Azure Security Center, usare questo cmdlet per visualizzare le soluzioni di sicurezza individuate</span><span class="sxs-lookup"><span data-stu-id="52ca9-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="52ca9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52ca9-110">EXAMPLES</span></span>

### <span data-ttu-id="52ca9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="52ca9-111">Example 1</span></span>
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

<span data-ttu-id="52ca9-112">Ottenere tutte le soluzioni di sicurezza individuate nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="52ca9-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="52ca9-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="52ca9-113">Example 2</span></span>
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

<span data-ttu-id="52ca9-114">Ottenere una soluzione di sicurezza individuata specifica</span><span class="sxs-lookup"><span data-stu-id="52ca9-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="52ca9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52ca9-115">PARAMETERS</span></span>

### <span data-ttu-id="52ca9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ca9-116">-DefaultProfile</span></span>
<span data-ttu-id="52ca9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52ca9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52ca9-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="52ca9-118">-Location</span></span>
<span data-ttu-id="52ca9-119">Posizione.</span><span class="sxs-lookup"><span data-stu-id="52ca9-119">Location.</span></span>

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

### <span data-ttu-id="52ca9-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="52ca9-120">-Name</span></span>
<span data-ttu-id="52ca9-121">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="52ca9-121">Resource name.</span></span>

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

### <span data-ttu-id="52ca9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52ca9-122">-ResourceGroupName</span></span>
<span data-ttu-id="52ca9-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="52ca9-123">Resource group name.</span></span>

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

### <span data-ttu-id="52ca9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52ca9-124">-ResourceId</span></span>
<span data-ttu-id="52ca9-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="52ca9-125">Resource ID.</span></span>

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

### <span data-ttu-id="52ca9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ca9-126">CommonParameters</span></span>
<span data-ttu-id="52ca9-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52ca9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ca9-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52ca9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ca9-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52ca9-129">INPUTS</span></span>

### <span data-ttu-id="52ca9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="52ca9-130">System.String</span></span>

## <span data-ttu-id="52ca9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52ca9-131">OUTPUTS</span></span>

### <span data-ttu-id="52ca9-132">Microsoft. Azure. Commands. Security. Models. DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="52ca9-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="52ca9-133">Note</span><span class="sxs-lookup"><span data-stu-id="52ca9-133">NOTES</span></span>

## <span data-ttu-id="52ca9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52ca9-134">RELATED LINKS</span></span>
