---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
ms.openlocfilehash: dc51caee3a0cb8d5571a5a316c2018c30abbe239
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522094"
---
# <span data-ttu-id="5e2ac-101">New-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="5e2ac-101">New-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="5e2ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="5e2ac-103">Crea un'istanza di PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="5e2ac-103">Creates an instance of PsApiManagementRegion.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e2ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e2ac-104">SYNTAX</span></span>

```
New-AzureRmApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e2ac-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e2ac-105">DESCRIPTION</span></span>
<span data-ttu-id="5e2ac-106">Comando helper per creare un'istanza di PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="5e2ac-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="5e2ac-107">Questo comando deve essere usato con il comando New-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="5e2ac-107">This command is to be used with New-AzureRmApiManagement command.</span></span>

## <span data-ttu-id="5e2ac-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e2ac-108">EXAMPLES</span></span>

### <span data-ttu-id="5e2ac-109">--------------------------Esempio 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5e2ac-109">--------------------------  Example 1  --------------------------</span></span>
```
$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="5e2ac-110">--------------------------Esempio 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="5e2ac-110">--------------------------  Example 2  --------------------------</span></span>
```
$apimRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="5e2ac-111">Crea un servizio ApiManagement di VpnType esterno nell'area ovest degli Stati Uniti, con un'area aggiuntiva nel centro degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="5e2ac-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="5e2ac-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e2ac-112">PARAMETERS</span></span>

### <span data-ttu-id="5e2ac-113">-Capacità</span><span class="sxs-lookup"><span data-stu-id="5e2ac-113">-Capacity</span></span>
<span data-ttu-id="5e2ac-114">Capacità SKU del servizio di gestione delle API di Azure altre aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="5e2ac-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="5e2ac-115">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="5e2ac-115">Default value is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e2ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e2ac-116">-DefaultProfile</span></span>
<span data-ttu-id="5e2ac-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e2ac-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="5e2ac-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5e2ac-118">-Location</span></span>
<span data-ttu-id="5e2ac-119">Specifica la posizione della nuova area di distribuzione tra l'area supportata per il servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="5e2ac-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="5e2ac-120">Per ottenere posizioni valide, usare il cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | dove {$ _. ResourceTypes [0]. ResourceTypeName-EQ "servizio"} | Posizioni Select-Object</span><span class="sxs-lookup"><span data-stu-id="5e2ac-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e2ac-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5e2ac-121">-VirtualNetwork</span></span>
<span data-ttu-id="5e2ac-122">Configurazione della rete virtuale dell'area di distribuzione di Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="5e2ac-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="5e2ac-123">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="5e2ac-123">Default value is $null.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e2ac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e2ac-124">CommonParameters</span></span>
<span data-ttu-id="5e2ac-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e2ac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e2ac-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e2ac-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e2ac-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e2ac-127">INPUTS</span></span>

### <span data-ttu-id="5e2ac-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5e2ac-128">None</span></span>
<span data-ttu-id="5e2ac-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5e2ac-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5e2ac-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e2ac-130">OUTPUTS</span></span>

### <span data-ttu-id="5e2ac-131">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="5e2ac-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="5e2ac-132">Note</span><span class="sxs-lookup"><span data-stu-id="5e2ac-132">NOTES</span></span>

## <span data-ttu-id="5e2ac-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e2ac-133">RELATED LINKS</span></span>

