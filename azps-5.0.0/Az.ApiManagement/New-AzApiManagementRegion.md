---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
ms.openlocfilehash: 2259990c568dbf6fd5b7bc6f8bff34c464a082ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200557"
---
# <span data-ttu-id="4e315-101">New-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="4e315-101">New-AzApiManagementRegion</span></span>

## <span data-ttu-id="4e315-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e315-102">SYNOPSIS</span></span>
<span data-ttu-id="4e315-103">Crea un'istanza di PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="4e315-103">Creates an instance of PsApiManagementRegion.</span></span>

## <span data-ttu-id="4e315-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e315-104">SYNTAX</span></span>

```
New-AzApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e315-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e315-105">DESCRIPTION</span></span>
<span data-ttu-id="4e315-106">Comando helper per creare un'istanza di PsApiManagementRegion.</span><span class="sxs-lookup"><span data-stu-id="4e315-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="4e315-107">Questo comando deve essere usato con il comando New-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="4e315-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="4e315-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e315-108">EXAMPLES</span></span>

### <span data-ttu-id="4e315-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e315-109">Example 1</span></span>
```
$apimRegion = New-AzApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="4e315-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4e315-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="4e315-111">Crea un servizio ApiManagement di VpnType esterno nell'area ovest degli Stati Uniti, con un'area aggiuntiva nel centro degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="4e315-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="4e315-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e315-112">PARAMETERS</span></span>

### <span data-ttu-id="4e315-113">-Capacità</span><span class="sxs-lookup"><span data-stu-id="4e315-113">-Capacity</span></span>
<span data-ttu-id="4e315-114">Capacità SKU del servizio di gestione delle API di Azure altre aree geografiche.</span><span class="sxs-lookup"><span data-stu-id="4e315-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="4e315-115">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="4e315-115">Default value is 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e315-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e315-116">-DefaultProfile</span></span>
<span data-ttu-id="4e315-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e315-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e315-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4e315-118">-Location</span></span>
<span data-ttu-id="4e315-119">Specifica la posizione della nuova area di distribuzione tra l'area supportata per il servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="4e315-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="4e315-120">Per ottenere posizioni valide, usare il cmdlet Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | dove {$ _. ResourceTypes [0]. ResourceTypeName-EQ "servizio"} | Posizioni Select-Object</span><span class="sxs-lookup"><span data-stu-id="4e315-120">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="4e315-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4e315-121">-VirtualNetwork</span></span>
<span data-ttu-id="4e315-122">Configurazione della rete virtuale dell'area di distribuzione di Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="4e315-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="4e315-123">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="4e315-123">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e315-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e315-124">CommonParameters</span></span>
<span data-ttu-id="4e315-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e315-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e315-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e315-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e315-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e315-127">INPUTS</span></span>

### <span data-ttu-id="4e315-128">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4e315-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="4e315-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e315-129">OUTPUTS</span></span>

### <span data-ttu-id="4e315-130">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="4e315-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="4e315-131">Note</span><span class="sxs-lookup"><span data-stu-id="4e315-131">NOTES</span></span>

## <span data-ttu-id="4e315-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e315-132">RELATED LINKS</span></span>