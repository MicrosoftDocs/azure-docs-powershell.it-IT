---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
ms.openlocfilehash: 1ab783b4b5a49793b4f4c91f2f7bc9f5410e5ddd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510432"
---
# <span data-ttu-id="23255-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="23255-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="23255-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23255-102">SYNOPSIS</span></span>
<span data-ttu-id="23255-103">Rimuove una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="23255-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23255-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23255-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23255-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23255-105">DESCRIPTION</span></span>
<span data-ttu-id="23255-106">Il cmdlet **Remove-AzureRmVirtualNetwork** rimuove una rete virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="23255-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="23255-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23255-107">EXAMPLES</span></span>

### <span data-ttu-id="23255-108">1: creare ed eliminare una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="23255-108">1: Create and delete a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="23255-109">Questo esempio crea una rete virtuale in un gruppo di risorse e quindi la Elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="23255-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="23255-110">Per eliminare la richiesta quando si elimina la rete virtuale, usare il contrassegno-forza.</span><span class="sxs-lookup"><span data-stu-id="23255-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="23255-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23255-111">PARAMETERS</span></span>

### <span data-ttu-id="23255-112">-Force</span><span class="sxs-lookup"><span data-stu-id="23255-112">-Force</span></span>
<span data-ttu-id="23255-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="23255-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23255-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="23255-114">-Name</span></span>
<span data-ttu-id="23255-115">Specifica il nome della rete virtuale rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23255-115">Specifies the name of the virtual network that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23255-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23255-116">-PassThru</span></span>
<span data-ttu-id="23255-117">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="23255-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="23255-118">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="23255-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23255-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23255-119">-ResourceGroupName</span></span>
<span data-ttu-id="23255-120">Specifica il nome del gruppo di risorse che contiene la rete virtuale rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23255-120">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23255-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="23255-121">-Confirm</span></span>
<span data-ttu-id="23255-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23255-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23255-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23255-123">-WhatIf</span></span>
<span data-ttu-id="23255-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23255-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23255-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23255-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23255-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23255-126">-DefaultProfile</span></span>
<span data-ttu-id="23255-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23255-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23255-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23255-128">CommonParameters</span></span>
<span data-ttu-id="23255-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23255-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23255-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23255-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23255-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23255-131">INPUTS</span></span>

## <span data-ttu-id="23255-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23255-132">OUTPUTS</span></span>

## <span data-ttu-id="23255-133">Note</span><span class="sxs-lookup"><span data-stu-id="23255-133">NOTES</span></span>

## <span data-ttu-id="23255-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23255-134">RELATED LINKS</span></span>

[<span data-ttu-id="23255-135">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="23255-135">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="23255-136">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="23255-136">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="23255-137">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="23255-137">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


