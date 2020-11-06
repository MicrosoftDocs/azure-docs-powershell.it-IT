---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmDiscoveredSecuritySolution.md
ms.openlocfilehash: ecea7ba6aa34df73de65a4d03e004531e81ff497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513455"
---
# <span data-ttu-id="aff58-101">Get-AzureRmDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="aff58-101">Get-AzureRmDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="aff58-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aff58-102">SYNOPSIS</span></span>
<span data-ttu-id="aff58-103">Ottiene soluzioni di sicurezza individuate da Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="aff58-103">Gets security solutions that were discovered by Azure Security Center</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aff58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aff58-104">SYNTAX</span></span>

### <span data-ttu-id="aff58-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aff58-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmDiscoveredSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aff58-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="aff58-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aff58-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="aff58-107">ResourceId</span></span>
```
Get-AzureRmDiscoveredSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aff58-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aff58-108">DESCRIPTION</span></span>
<span data-ttu-id="aff58-109">Le soluzioni di sicurezza vengono scoperte automaticamente da Azure Security Center, usare questo cmdlet per visualizzare le soluzioni di sicurezza individuate</span><span class="sxs-lookup"><span data-stu-id="aff58-109">Security solutions are automatically discovered by Azure Security Center, use this cmdlet to view the discovered security solutions</span></span>

## <span data-ttu-id="aff58-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aff58-110">EXAMPLES</span></span>

### <span data-ttu-id="aff58-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aff58-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="aff58-112">Ottenere tutte le soluzioni di sicurezza individuate nell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="aff58-112">Get all the discovered security solutions in the subscription</span></span>

### <span data-ttu-id="aff58-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="aff58-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmDiscoveredSecuritySolution -ResourceGroupName "myService1" -Location "centralus" -Name "ContosoWAF2"
Id             : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Secu
                 rity/locations/centralus/discoveredSecuritySolutions/ContosoWAF2
Name           : ContosoWAF2
Offer          : 
Publisher      : microsoft
SecurityFamily : SaasWaf
Sku            :
```

<span data-ttu-id="aff58-114">Ottenere una soluzione di sicurezza individuata specifica</span><span class="sxs-lookup"><span data-stu-id="aff58-114">Get a specific discovered security solution</span></span>

## <span data-ttu-id="aff58-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aff58-115">PARAMETERS</span></span>

### <span data-ttu-id="aff58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff58-116">-DefaultProfile</span></span>
<span data-ttu-id="aff58-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aff58-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff58-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="aff58-118">-Location</span></span>
<span data-ttu-id="aff58-119">Posizione.</span><span class="sxs-lookup"><span data-stu-id="aff58-119">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff58-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="aff58-120">-Name</span></span>
<span data-ttu-id="aff58-121">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="aff58-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff58-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aff58-122">-ResourceGroupName</span></span>
<span data-ttu-id="aff58-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aff58-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aff58-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aff58-124">-ResourceId</span></span>
<span data-ttu-id="aff58-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="aff58-125">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aff58-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff58-126">CommonParameters</span></span>
<span data-ttu-id="aff58-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aff58-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff58-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aff58-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff58-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aff58-129">INPUTS</span></span>

### <span data-ttu-id="aff58-130">System. String</span><span class="sxs-lookup"><span data-stu-id="aff58-130">System.String</span></span>

## <span data-ttu-id="aff58-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aff58-131">OUTPUTS</span></span>

### <span data-ttu-id="aff58-132">Microsoft. Azure. Commands. Security. Models. DiscoveredSecuritySolutions. PSSecurityDiscoveredSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="aff58-132">Microsoft.Azure.Commands.Security.Models.DiscoveredSecuritySolutions.PSSecurityDiscoveredSecuritySolution</span></span>

## <span data-ttu-id="aff58-133">Note</span><span class="sxs-lookup"><span data-stu-id="aff58-133">NOTES</span></span>

## <span data-ttu-id="aff58-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aff58-134">RELATED LINKS</span></span>
