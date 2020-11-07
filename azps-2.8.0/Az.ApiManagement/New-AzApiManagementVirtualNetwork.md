---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 8833d6380c14c3b2e9b9c53657602f9f3cbfd1af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675972"
---
# <span data-ttu-id="0ebf4-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0ebf4-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="0ebf4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ebf4-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebf4-103">Crea un'istanza di PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="0ebf4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ebf4-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ebf4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ebf4-105">DESCRIPTION</span></span>
<span data-ttu-id="0ebf4-106">Il cmdlet **New-AzApiManagementVirtualNetwork** è un comando helper per creare un'istanza di **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="0ebf4-107">Questo comando viene usato con i cmdlet **set-AzApiManagement** e **New-AzApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="0ebf4-107">This command is used with **Set-AzApiManagement** and **New-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="0ebf4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ebf4-108">EXAMPLES</span></span>

### <span data-ttu-id="0ebf4-109">Esempio 1: creare una rete virtuale e aggiornare un servizio APIM esistente in VNET</span><span class="sxs-lookup"><span data-stu-id="0ebf4-109">Example 1: Create a virtual network and Update an existing APIM service into the VNET</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="0ebf4-110">Questo esempio crea una rete virtuale e quindi chiama il cmdlet **set-AzApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="0ebf4-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

### <span data-ttu-id="0ebf4-111">Esempio 2: creare un servizio di gestione delle API per una rete virtuale esterna</span><span class="sxs-lookup"><span data-stu-id="0ebf4-111">Example 2: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="0ebf4-112">Questo esempio crea un nuovo servizio APIM in una rete virtuale in `External` modalità</span><span class="sxs-lookup"><span data-stu-id="0ebf4-112">This example creates a new APIM service into a Virtual Network in `External` mode</span></span>

## <span data-ttu-id="0ebf4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ebf4-113">PARAMETERS</span></span>

### <span data-ttu-id="0ebf4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebf4-114">-DefaultProfile</span></span>
<span data-ttu-id="0ebf4-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ebf4-116">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="0ebf4-116">-SubnetResourceId</span></span>
<span data-ttu-id="0ebf4-117">Specifica l'ID della risorsa subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-117">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="0ebf4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebf4-118">CommonParameters</span></span>
<span data-ttu-id="0ebf4-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebf4-120">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ebf4-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebf4-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ebf4-121">INPUTS</span></span>

### <span data-ttu-id="0ebf4-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0ebf4-122">None</span></span>

## <span data-ttu-id="0ebf4-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ebf4-123">OUTPUTS</span></span>

### <span data-ttu-id="0ebf4-124">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0ebf4-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="0ebf4-125">Note</span><span class="sxs-lookup"><span data-stu-id="0ebf4-125">NOTES</span></span>

## <span data-ttu-id="0ebf4-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ebf4-126">RELATED LINKS</span></span>

<span data-ttu-id="0ebf4-127">[Set-AzApiManagement](./Set-AzApiManagement.md) 
 [New-AzApiManagement](./New-AzApiManagement.md)</span><span class="sxs-lookup"><span data-stu-id="0ebf4-127">[Set-AzApiManagement](./Set-AzApiManagement.md)
[New-AzApiManagement](./New-AzApiManagement.md)</span></span>

