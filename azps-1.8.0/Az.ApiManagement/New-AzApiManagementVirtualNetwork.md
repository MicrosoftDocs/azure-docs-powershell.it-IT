---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 67020f99129dfa920aa1bbc5e22ac59c16affb32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852509"
---
# <span data-ttu-id="56d5c-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="56d5c-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="56d5c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="56d5c-103">Crea un'istanza di PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="56d5c-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="56d5c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56d5c-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56d5c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56d5c-105">DESCRIPTION</span></span>
<span data-ttu-id="56d5c-106">Il cmdlet **New-AzApiManagementVirtualNetwork** è un comando helper per creare un'istanza di **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="56d5c-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="56d5c-107">Questo comando viene usato con il cmdlet **Update-AzApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="56d5c-107">This command is used with **Update-AzApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="56d5c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56d5c-108">EXAMPLES</span></span>

### <span data-ttu-id="56d5c-109">Esempio 1: creare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="56d5c-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="56d5c-110">Questo esempio crea una rete virtuale e quindi chiama il cmdlet **Update-AzApiManagementDeployment** .</span><span class="sxs-lookup"><span data-stu-id="56d5c-110">This example creates a virtual network and then calls the **Update-AzApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="56d5c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56d5c-111">PARAMETERS</span></span>

### <span data-ttu-id="56d5c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d5c-112">-DefaultProfile</span></span>
<span data-ttu-id="56d5c-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56d5c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56d5c-114">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="56d5c-114">-SubnetResourceId</span></span>
<span data-ttu-id="56d5c-115">Specifica l'ID della risorsa subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="56d5c-115">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="56d5c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d5c-116">CommonParameters</span></span>
<span data-ttu-id="56d5c-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56d5c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d5c-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56d5c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d5c-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56d5c-119">INPUTS</span></span>

### <span data-ttu-id="56d5c-120">Nessuno</span><span class="sxs-lookup"><span data-stu-id="56d5c-120">None</span></span>

## <span data-ttu-id="56d5c-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56d5c-121">OUTPUTS</span></span>

### <span data-ttu-id="56d5c-122">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="56d5c-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="56d5c-123">Note</span><span class="sxs-lookup"><span data-stu-id="56d5c-123">NOTES</span></span>

## <span data-ttu-id="56d5c-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56d5c-124">RELATED LINKS</span></span>

[<span data-ttu-id="56d5c-125">Update-AzApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="56d5c-125">Update-AzApiManagementDeployment</span></span>](./Update-AzApiManagementDeployment.md)

