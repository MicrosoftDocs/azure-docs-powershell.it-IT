---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 30a237f0f87286be8f6cd18e804d80850df7a8be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522092"
---
# <span data-ttu-id="61907-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="61907-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="61907-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="61907-102">SYNOPSIS</span></span>
<span data-ttu-id="61907-103">Crea un'istanza di PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="61907-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61907-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="61907-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61907-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="61907-105">DESCRIPTION</span></span>
<span data-ttu-id="61907-106">Il cmdlet **New-AzureRmApiManagementVirtualNetwork** è un comando helper per creare un'istanza di **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="61907-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="61907-107">Questo comando viene usato con il cmdlet **Update-AzureRmApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="61907-107">This command is used with **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="61907-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="61907-108">EXAMPLES</span></span>

### <span data-ttu-id="61907-109">Esempio 1: creare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="61907-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzureRmvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzureRmApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzureRmApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="61907-110">Questo esempio crea una rete virtuale e quindi chiama il cmdlet **Update-AzureRmApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="61907-110">This example creates a virtual network and then calls the **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="61907-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="61907-111">PARAMETERS</span></span>

### <span data-ttu-id="61907-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61907-112">-DefaultProfile</span></span>
<span data-ttu-id="61907-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="61907-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="61907-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="61907-114">-Location</span></span>
<span data-ttu-id="61907-115">Specifica la posizione tra l'area supportata per il servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="61907-115">Specifies the location amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="61907-116">Per ottenere posizioni valide, usare il cmdlet Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | dove {$ _. ResourceTypes [0]. ResourceTypeName-EQ "servizio"} | Posizioni Select-Object</span><span class="sxs-lookup"><span data-stu-id="61907-116">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="61907-117">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="61907-117">-SubnetResourceId</span></span>
<span data-ttu-id="61907-118">Specifica l'ID della risorsa subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="61907-118">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="61907-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61907-119">CommonParameters</span></span>
<span data-ttu-id="61907-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61907-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61907-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61907-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61907-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="61907-122">INPUTS</span></span>

### <span data-ttu-id="61907-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="61907-123">None</span></span>
<span data-ttu-id="61907-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="61907-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61907-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="61907-125">OUTPUTS</span></span>

### <span data-ttu-id="61907-126">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="61907-126">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="61907-127">Note</span><span class="sxs-lookup"><span data-stu-id="61907-127">NOTES</span></span>

## <span data-ttu-id="61907-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="61907-128">RELATED LINKS</span></span>

[<span data-ttu-id="61907-129">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="61907-129">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)

