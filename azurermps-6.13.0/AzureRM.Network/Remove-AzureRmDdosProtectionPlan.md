---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 87110fe779e128e8ef5d5d6de0504ec9fdca1b25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521815"
---
# <span data-ttu-id="dd2cd-101">Remove-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="dd2cd-101">Remove-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="dd2cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd2cd-102">SYNOPSIS</span></span>
<span data-ttu-id="dd2cd-103">Rimuove un piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-103">Removes a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd2cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd2cd-104">SYNTAX</span></span>

```
Remove-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd2cd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd2cd-105">DESCRIPTION</span></span>
<span data-ttu-id="dd2cd-106">Il cmdlet Remove-AzureRmDdosProtectionPlan rimuove un piano di protezione DDoS.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-106">The Remove-AzureRmDdosProtectionPlan cmdlet removes a DDoS protection plan.</span></span>

## <span data-ttu-id="dd2cd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd2cd-107">EXAMPLES</span></span>

### <span data-ttu-id="dd2cd-108">Esempio 1: rimuovere un piano di protezione DDoS vuoto</span><span class="sxs-lookup"><span data-stu-id="dd2cd-108">Example 1: Remove an empty DDoS protection plan</span></span>
```
D:\> Remove-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="dd2cd-109">In questo caso, rimuoviamo un piano di protezione DDoS come specificato.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-109">In this case, we remove a DDoS protection plan as specified.</span></span>

### <span data-ttu-id="dd2cd-110">Esempio 2: rimuovere un piano di protezione DDoS associato a una rete virtuale</span><span class="sxs-lookup"><span data-stu-id="dd2cd-110">Example 2: Remove a DDoS protection plan associated with a virtual network</span></span>
```
D:\> $vnet = Get-AzureRmVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = $null
D:\> $vnet.EnableDdosProtection = $false
D:\> $vnet | Set-AzureRmVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"65947351-747e-4686-aa8b-c40da58f6c8b"
ResourceGuid           : fcb7bc1e-ee0d-4005-b3f1-feda76e3756c
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "10.0.0.0/16"
                           ]
                         }
DhcpOptions            : {
                           "DnsServers": [
                             "8.8.8.8"
                           ]
                         }
Subnets                : [
                           {
                             "Name": "SubnetName",
                             "Etag": "W/\"65947351-747e-4686-aa8b-c40da58f6c8b\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
EnableVmProtection     : false


D:\> Remove-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="dd2cd-111">I piani di protezione DDoS non possono essere eliminati se associati a una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-111">DDoS protection plans cannot be deleted if they are associated with a virtual network.</span></span> <span data-ttu-id="dd2cd-112">Il primo passaggio consiste nel disassociare entrambi gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-112">So the first step is to disassociate both objects.</span></span> <span data-ttu-id="dd2cd-113">Qui otteniamo la versione più aggiornata della rete virtuale associata al piano e impostiamo la proprietà **DdosProtectionPlan** su un valore vuoto e il contrassegno **EnableDdosProtection** (questo contrassegno non può essere vero senza un piano).</span><span class="sxs-lookup"><span data-stu-id="dd2cd-113">Here, we get the most updated version of the virtual network associated with the plan, and we set the property **DdosProtectionPlan** to an empty value and the flag **EnableDdosProtection** (this flag cannot be true without a plan).</span></span>
<span data-ttu-id="dd2cd-114">Quindi, persistiamo il nuovo stato eseguendo il piping della variabile locale in **set-AzureRmVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-114">Then, we persist the new state by piping the local variable into **Set-AzureRmVirtualNetwork**.</span></span> <span data-ttu-id="dd2cd-115">A questo punto, il piano non è più associato alla rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-115">At this point, the plan is no longer associated with the virtual network.</span></span>
<span data-ttu-id="dd2cd-116">Se questa è l'ultima associata al piano, è possibile rimuovere il piano di protezione DDoS usando il comando Rimuovi-AzureRmDdosProtectionPlan.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-116">If this is the last one associated with the plan, we can remove the DDoS protection plan by using the command Remove-AzureRmDdosProtectionPlan.</span></span>

## <span data-ttu-id="dd2cd-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd2cd-117">PARAMETERS</span></span>

### <span data-ttu-id="dd2cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd2cd-118">-DefaultProfile</span></span>
<span data-ttu-id="dd2cd-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd2cd-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd2cd-120">-Name</span></span>
<span data-ttu-id="dd2cd-121">Specifica il nome del piano di protezione DDoS da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-121">Specifies the name of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="dd2cd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd2cd-122">-PassThru</span></span>
<span data-ttu-id="dd2cd-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dd2cd-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dd2cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd2cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="dd2cd-126">Specifica il gruppo di risorse del piano di protezione DDoS da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-126">Specifies the resource group of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="dd2cd-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dd2cd-127">-Confirm</span></span>
<span data-ttu-id="dd2cd-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2cd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd2cd-129">-WhatIf</span></span>
<span data-ttu-id="dd2cd-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd2cd-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2cd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd2cd-132">CommonParameters</span></span>
<span data-ttu-id="dd2cd-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd2cd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd2cd-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd2cd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd2cd-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd2cd-135">INPUTS</span></span>

### <span data-ttu-id="dd2cd-136">System. String</span><span class="sxs-lookup"><span data-stu-id="dd2cd-136">System.String</span></span>

## <span data-ttu-id="dd2cd-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd2cd-137">OUTPUTS</span></span>

### <span data-ttu-id="dd2cd-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd2cd-138">System.Boolean</span></span>

## <span data-ttu-id="dd2cd-139">Note</span><span class="sxs-lookup"><span data-stu-id="dd2cd-139">NOTES</span></span>

## <span data-ttu-id="dd2cd-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd2cd-140">RELATED LINKS</span></span>

[<span data-ttu-id="dd2cd-141">New-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="dd2cd-141">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="dd2cd-142">Get-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="dd2cd-142">Get-AzureRmDdosProtectionPlan</span></span>](./Get-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="dd2cd-143">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dd2cd-143">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="dd2cd-144">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dd2cd-144">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="dd2cd-145">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dd2cd-145">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
