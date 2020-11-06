---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 42213ddd4a7780b4d69b357c4b801df34aa9aca4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508831"
---
# <span data-ttu-id="c49b1-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c49b1-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="c49b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c49b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c49b1-103">Crea un'istanza di PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="c49b1-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c49b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c49b1-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c49b1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c49b1-105">DESCRIPTION</span></span>
<span data-ttu-id="c49b1-106">Il cmdlet **New-AzureRmApiManagementVirtualNetwork** è un comando helper per creare un'istanza di **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="c49b1-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="c49b1-107">Questo comando viene usato con il cmdlet **set-AzureRMApiManagementVirtualNetworks** .</span><span class="sxs-lookup"><span data-stu-id="c49b1-107">This command is used with **Set-AzureRMApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="c49b1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c49b1-108">EXAMPLES</span></span>

### <span data-ttu-id="c49b1-109">Esempio 1: creare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c49b1-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$VirtualNetworks = @()
PS C:\> $VirtualNetworks += New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubtenName "ContosoNet" -VnetId "089D3F4D-B986-4DFD-9259-9112BA7A1F03"
PS C:\> Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $VirtualNetworks
```

<span data-ttu-id="c49b1-110">Questo esempio crea una rete virtuale e quindi chiama il cmdlet **set-AzureRmApiManagementVirtualNetworks** .</span><span class="sxs-lookup"><span data-stu-id="c49b1-110">This example creates a virtual network and then calls the **Set-AzureRmApiManagementVirtualNetworks** cmdlet.</span></span>

## <span data-ttu-id="c49b1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c49b1-111">PARAMETERS</span></span>

### <span data-ttu-id="c49b1-112">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c49b1-112">-Location</span></span>
<span data-ttu-id="c49b1-113">Specifica la posizione della rete virtuale in cui questo cmdlet crea l'istanza.</span><span class="sxs-lookup"><span data-stu-id="c49b1-113">Specifies the location of the virtual network in which this cmdlet creates the instance.</span></span>

<span data-ttu-id="c49b1-114">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c49b1-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c49b1-115">Stati Uniti nord-centrale</span><span class="sxs-lookup"><span data-stu-id="c49b1-115">North Central US</span></span>
- <span data-ttu-id="c49b1-116">Stati Uniti del centro sud</span><span class="sxs-lookup"><span data-stu-id="c49b1-116">South Central US</span></span>
- <span data-ttu-id="c49b1-117">Stati Uniti centrali</span><span class="sxs-lookup"><span data-stu-id="c49b1-117">Central US</span></span>
- <span data-ttu-id="c49b1-118">Europa occidentale</span><span class="sxs-lookup"><span data-stu-id="c49b1-118">West Europe</span></span>
- <span data-ttu-id="c49b1-119">Nord Europa</span><span class="sxs-lookup"><span data-stu-id="c49b1-119">North Europe</span></span>
- <span data-ttu-id="c49b1-120">Ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="c49b1-120">West US</span></span>
- <span data-ttu-id="c49b1-121">Stati Uniti orientali</span><span class="sxs-lookup"><span data-stu-id="c49b1-121">East US</span></span>
- <span data-ttu-id="c49b1-122">Stati Uniti Est 2</span><span class="sxs-lookup"><span data-stu-id="c49b1-122">East US 2</span></span>
- <span data-ttu-id="c49b1-123">Giappone est</span><span class="sxs-lookup"><span data-stu-id="c49b1-123">Japan East</span></span>
- <span data-ttu-id="c49b1-124">Giappone ovest</span><span class="sxs-lookup"><span data-stu-id="c49b1-124">Japan West</span></span>
- <span data-ttu-id="c49b1-125">Brasile sud</span><span class="sxs-lookup"><span data-stu-id="c49b1-125">Brazil South</span></span>
- <span data-ttu-id="c49b1-126">Asia sud-orientale</span><span class="sxs-lookup"><span data-stu-id="c49b1-126">Southeast Asia</span></span>
- <span data-ttu-id="c49b1-127">Asia orientale</span><span class="sxs-lookup"><span data-stu-id="c49b1-127">East Asia</span></span>
- <span data-ttu-id="c49b1-128">Australia Est</span><span class="sxs-lookup"><span data-stu-id="c49b1-128">Australia East</span></span>
- <span data-ttu-id="c49b1-129">Australia sud-est</span><span class="sxs-lookup"><span data-stu-id="c49b1-129">Australia Southeast</span></span>

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

### <span data-ttu-id="c49b1-130">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="c49b1-130">-SubnetResourceId</span></span>
<span data-ttu-id="c49b1-131">Specifica l'ID della risorsa subnet della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="c49b1-131">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="c49b1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c49b1-132">-DefaultProfile</span></span>
<span data-ttu-id="c49b1-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c49b1-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c49b1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c49b1-134">CommonParameters</span></span>
<span data-ttu-id="c49b1-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c49b1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c49b1-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c49b1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c49b1-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c49b1-137">INPUTS</span></span>

## <span data-ttu-id="c49b1-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c49b1-138">OUTPUTS</span></span>

### <span data-ttu-id="c49b1-139">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c49b1-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="c49b1-140">Note</span><span class="sxs-lookup"><span data-stu-id="c49b1-140">NOTES</span></span>

## <span data-ttu-id="c49b1-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c49b1-141">RELATED LINKS</span></span>

