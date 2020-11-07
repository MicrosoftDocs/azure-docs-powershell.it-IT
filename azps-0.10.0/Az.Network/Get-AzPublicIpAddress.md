---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: b9eaacb9a9d779814fc5f0b873aa8e98afedd362
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860685"
---
# <span data-ttu-id="a3ff9-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a3ff9-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="a3ff9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ff9-103">Ottiene un indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="a3ff9-103">Gets a public IP address.</span></span>

## <span data-ttu-id="a3ff9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3ff9-104">SYNTAX</span></span>

### <span data-ttu-id="a3ff9-105">NoExpandStandAloneIp (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a3ff9-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3ff9-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="a3ff9-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3ff9-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="a3ff9-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3ff9-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="a3ff9-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3ff9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3ff9-109">DESCRIPTION</span></span>
<span data-ttu-id="a3ff9-110">Il cmdlet **Get-AzPublicIPAddress** ottiene uno o più indirizzi IP pubblici in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a3ff9-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="a3ff9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3ff9-111">EXAMPLES</span></span>

### <span data-ttu-id="a3ff9-112">1: ottenere una risorsa IP pubblica</span><span class="sxs-lookup"><span data-stu-id="a3ff9-112">1: Get a public IP resource</span></span>
```
$publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName $publicIp
```

<span data-ttu-id="a3ff9-113">Questo comando consente di ottenere una risorsa indirizzo IP pubblico con nome $publicIPName nel gruppo risorse $rgName.</span><span class="sxs-lookup"><span data-stu-id="a3ff9-113">This command gets a public IP address resource with name $publicIPName in the resource group $rgName.</span></span>

## <span data-ttu-id="a3ff9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3ff9-114">PARAMETERS</span></span>

### <span data-ttu-id="a3ff9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ff9-115">-DefaultProfile</span></span>
<span data-ttu-id="a3ff9-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3ff9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3ff9-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="a3ff9-117">-ExpandResource</span></span>
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

### <span data-ttu-id="a3ff9-118">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a3ff9-118">-IpConfigurationName</span></span>
<span data-ttu-id="a3ff9-119">Nome della configurazione dell'interfaccia di rete IP.</span><span class="sxs-lookup"><span data-stu-id="a3ff9-119">Network Interface IP Configuration Name.</span></span>
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

### <span data-ttu-id="a3ff9-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3ff9-120">-Name</span></span>
<span data-ttu-id="a3ff9-121">Specifica il nome dell'indirizzo IP pubblico ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3ff9-121">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a3ff9-122">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="a3ff9-122">-NetworkInterfaceName</span></span>
<span data-ttu-id="a3ff9-123">Nome dell'interfaccia di rete della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a3ff9-123">Virtual Machine Network Interface Name.</span></span>
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

### <span data-ttu-id="a3ff9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3ff9-124">-ResourceGroupName</span></span>
<span data-ttu-id="a3ff9-125">Specifica il nome del gruppo di risorse che contiene l'indirizzo IP pubblico ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3ff9-125">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a3ff9-126">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="a3ff9-126">-VirtualMachineIndex</span></span>
<span data-ttu-id="a3ff9-127">Indice della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a3ff9-127">Virtual Machine Index.</span></span>
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

### <span data-ttu-id="a3ff9-128">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a3ff9-128">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="a3ff9-129">Nome set scala macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a3ff9-129">Virtual Machine Scale Set Name.</span></span>
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

### <span data-ttu-id="a3ff9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ff9-130">CommonParameters</span></span>
<span data-ttu-id="a3ff9-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3ff9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ff9-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3ff9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ff9-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3ff9-133">INPUTS</span></span>

## <span data-ttu-id="a3ff9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3ff9-134">OUTPUTS</span></span>

### <span data-ttu-id="a3ff9-135">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a3ff9-135">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="a3ff9-136">Note</span><span class="sxs-lookup"><span data-stu-id="a3ff9-136">NOTES</span></span>

## <span data-ttu-id="a3ff9-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3ff9-137">RELATED LINKS</span></span>

[<span data-ttu-id="a3ff9-138">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a3ff9-138">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="a3ff9-139">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a3ff9-139">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="a3ff9-140">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="a3ff9-140">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


