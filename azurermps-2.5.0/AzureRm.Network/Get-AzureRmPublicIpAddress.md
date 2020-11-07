---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: 1404acfa32de79096e990adbe2f66b43af0d4e96
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867030"
---
# <span data-ttu-id="063ee-101">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="063ee-101">Get-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="063ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="063ee-102">SYNOPSIS</span></span>
<span data-ttu-id="063ee-103">Ottiene un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="063ee-103">Gets a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="063ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="063ee-104">SYNTAX</span></span>

### <span data-ttu-id="063ee-105">NoExpandStandAloneIp (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="063ee-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="063ee-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="063ee-106">ExpandStandAloneIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="063ee-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="063ee-107">NoExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="063ee-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="063ee-108">ExpandScaleSetIp</span></span>
```
Get-AzureRmPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="063ee-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="063ee-109">DESCRIPTION</span></span>
<span data-ttu-id="063ee-110">Il cmdlet **Get-AzureRmPublicIPAddress** ottiene uno o più indirizzi IP pubblici in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="063ee-110">The **Get-AzureRmPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="063ee-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="063ee-111">EXAMPLES</span></span>

### <span data-ttu-id="063ee-112">1: ottenere una risorsa IP pubblica</span><span class="sxs-lookup"><span data-stu-id="063ee-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="063ee-113">Questo comando consente di ottenere una risorsa indirizzo IP pubblico con nome $publicIPName nel gruppo risorse $rgName.</span><span class="sxs-lookup"><span data-stu-id="063ee-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="063ee-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="063ee-114">PARAMETERS</span></span>

### <span data-ttu-id="063ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="063ee-115">-DefaultProfile</span></span>
<span data-ttu-id="063ee-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="063ee-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="063ee-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="063ee-117">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="063ee-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="063ee-118">-IpConfigurationName</span></span>
<span data-ttu-id="063ee-119">Nome della configurazione dell'interfaccia di rete IP.</span><span class="sxs-lookup"><span data-stu-id="063ee-119">Network Interface IP Configuration Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="063ee-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="063ee-120">-Name</span></span>
<span data-ttu-id="063ee-121">Specifica il nome dell'indirizzo IP pubblico ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="063ee-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="063ee-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="063ee-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="063ee-123">Nome dell'interfaccia di rete della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="063ee-123">Virtual Machine Network Interface Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="063ee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="063ee-124">-ResourceGroupName</span></span>
<span data-ttu-id="063ee-125">Specifica il nome del gruppo di risorse che contiene l'indirizzo IP pubblico ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="063ee-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpandStandAloneIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="063ee-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="063ee-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="063ee-127">Indice della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="063ee-127">Virtual Machine Index.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="063ee-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="063ee-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="063ee-129">Nome set scala macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="063ee-129">Virtual Machine Scale Set Name.</span></span>
```yaml
Type: String
Parameter Sets: NoExpandScaleSetIp
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ExpandScaleSetIp
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="063ee-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="063ee-130">CommonParameters</span></span>
<span data-ttu-id="063ee-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="063ee-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="063ee-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="063ee-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="063ee-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="063ee-133">INPUTS</span></span>

## <span data-ttu-id="063ee-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="063ee-134">OUTPUTS</span></span>

### <span data-ttu-id="063ee-135">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="063ee-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="063ee-136">Note</span><span class="sxs-lookup"><span data-stu-id="063ee-136">NOTES</span></span>

## <span data-ttu-id="063ee-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="063ee-137">RELATED LINKS</span></span>

[<span data-ttu-id="063ee-138">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="063ee-138">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="063ee-139">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="063ee-139">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)

[<span data-ttu-id="063ee-140">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="063ee-140">Set-AzureRmPublicIpAddress</span></span>](./Set-AzureRmPublicIpAddress.md)


