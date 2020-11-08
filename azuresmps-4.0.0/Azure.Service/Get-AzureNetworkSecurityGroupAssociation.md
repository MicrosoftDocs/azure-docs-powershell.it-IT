---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 6AF7D392-8C8B-4695-95D0-E927093F654A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21eb1b7bcad200e67659f830bfb3bbef42fe0f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94030044"
---
# <span data-ttu-id="153aa-101">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="153aa-101">Get-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="153aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="153aa-102">SYNOPSIS</span></span>
<span data-ttu-id="153aa-103">Ottiene un gruppo di sicurezza di rete per una macchina virtuale, una scheda di rete o un ruolo PaaS.</span><span class="sxs-lookup"><span data-stu-id="153aa-103">Gets a network security group for a virtual machine, network adapter, or PaaS role.</span></span>

## <span data-ttu-id="153aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="153aa-104">SYNTAX</span></span>

### <span data-ttu-id="153aa-105">GetNetworkSecurityGroupAssociationForSubnet</span><span class="sxs-lookup"><span data-stu-id="153aa-105">GetNetworkSecurityGroupAssociationForSubnet</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="153aa-106">GetNetworkSecurityGroupAssociationForIaaSRole</span><span class="sxs-lookup"><span data-stu-id="153aa-106">GetNetworkSecurityGroupAssociationForIaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="153aa-107">GetNetworkSecurityGroupAssociationForPaaSRole</span><span class="sxs-lookup"><span data-stu-id="153aa-107">GetNetworkSecurityGroupAssociationForPaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation [-Slot <String>] -RoleName <String> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="153aa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="153aa-108">DESCRIPTION</span></span>
<span data-ttu-id="153aa-109">Il cmdlet **Get-AzureNetworkSecurityGroupAssociation** ottiene il gruppo di sicurezza di rete per una macchina virtuale, una scheda di rete o un ruolo PaaS (Platform as a Service).</span><span class="sxs-lookup"><span data-stu-id="153aa-109">The **Get-AzureNetworkSecurityGroupAssociation** cmdlet gets the network security group for a virtual machine, network adapter, or platform as a service (PaaS) role.</span></span>

## <span data-ttu-id="153aa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="153aa-110">EXAMPLES</span></span>

### <span data-ttu-id="153aa-111">Esempio 1: ottenere il gruppo di sicurezza della rete per una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="153aa-111">Example 1: Get the network security group for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureNetworkSecurityGroupAssociation
```

<span data-ttu-id="153aa-112">Questo comando ottiene una macchina virtuale denominata ContosoVM06 per il servizio denominato ContosoService e passa l'oggetto macchina virtuale al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="153aa-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="153aa-113">Il cmdlet corrente ottiene il gruppo di sicurezza di rete associato alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="153aa-113">The current cmdlet gets the network security group associated to that virtual machine.</span></span>

## <span data-ttu-id="153aa-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="153aa-114">PARAMETERS</span></span>

### <span data-ttu-id="153aa-115">-Dettagli</span><span class="sxs-lookup"><span data-stu-id="153aa-115">-Detailed</span></span>
<span data-ttu-id="153aa-116">Indica che questo cmdlet restituisce i dettagli del gruppo di sicurezza di rete associato alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="153aa-116">Indicates that this cmdlet returns details of the network security group that is associated to the virtual machine.</span></span>
<span data-ttu-id="153aa-117">Questi dettagli includono posizione e regole.</span><span class="sxs-lookup"><span data-stu-id="153aa-117">These details include location and rules.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153aa-118">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="153aa-118">-NetworkInterfaceName</span></span>
<span data-ttu-id="153aa-119">Specifica il nome della scheda di rete per cui questo cmdlet ottiene il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="153aa-119">Specifies the name of the network adapter for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153aa-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="153aa-120">-Profile</span></span>
<span data-ttu-id="153aa-121">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="153aa-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="153aa-122">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="153aa-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153aa-123">-RoleName</span><span class="sxs-lookup"><span data-stu-id="153aa-123">-RoleName</span></span>
<span data-ttu-id="153aa-124">Specifica il nome di un ruolo PaaS per il quale questo cmdlet ottiene il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="153aa-124">Specifies the name of a PaaS role for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153aa-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="153aa-125">-ServiceName</span></span>
<span data-ttu-id="153aa-126">Specifica il nome di un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="153aa-126">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="153aa-127">Il ruolo PaaS appartiene al servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="153aa-127">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="153aa-128">-Slot</span><span class="sxs-lookup"><span data-stu-id="153aa-128">-Slot</span></span>
<span data-ttu-id="153aa-129">Specifica uno slot PaaS.</span><span class="sxs-lookup"><span data-stu-id="153aa-129">Specifies a PaaS slot.</span></span>
<span data-ttu-id="153aa-130">Il ruolo PaaS per cui questo cmdlet ottiene il gruppo di sicurezza di rete ha lo slot specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="153aa-130">The PaaS role for which this cmdlet gets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="153aa-131">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="153aa-131">Valid values are:</span></span> 

- <span data-ttu-id="153aa-132">Produzione</span><span class="sxs-lookup"><span data-stu-id="153aa-132">Production</span></span>
- <span data-ttu-id="153aa-133">Gestione temporanea</span><span class="sxs-lookup"><span data-stu-id="153aa-133">Staging</span></span> 

<span data-ttu-id="153aa-134">Il valore predefinito è Production.</span><span class="sxs-lookup"><span data-stu-id="153aa-134">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153aa-135">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="153aa-135">-SubnetName</span></span>
<span data-ttu-id="153aa-136">Specifica il nome di una subnet per cui questo cmdlet ottiene il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="153aa-136">Specifies the name of a subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153aa-137">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="153aa-137">-VirtualNetworkName</span></span>
<span data-ttu-id="153aa-138">Specifica il nome di una rete virtuale che contiene la subnet per cui questo cmdlet ottiene il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="153aa-138">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="153aa-139">-VM</span><span class="sxs-lookup"><span data-stu-id="153aa-139">-VM</span></span>
<span data-ttu-id="153aa-140">Specifica la macchina virtuale a cui questo cmdlet applica il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="153aa-140">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="153aa-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="153aa-141">CommonParameters</span></span>
<span data-ttu-id="153aa-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="153aa-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="153aa-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="153aa-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="153aa-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="153aa-144">INPUTS</span></span>

## <span data-ttu-id="153aa-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="153aa-145">OUTPUTS</span></span>

### <span data-ttu-id="153aa-146">Microsoft. WindowsAzure. Commands. ServiceManagement. Network. NetworkSecurityGroup. Model. INetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="153aa-146">Microsoft.WindowsAzure.Commands.ServiceManagement.Network.NetworkSecurityGroup.Model.INetworkSecurityGroup</span></span>

## <span data-ttu-id="153aa-147">Note</span><span class="sxs-lookup"><span data-stu-id="153aa-147">NOTES</span></span>

## <span data-ttu-id="153aa-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="153aa-148">RELATED LINKS</span></span>

[<span data-ttu-id="153aa-149">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="153aa-149">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="153aa-150">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="153aa-150">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)


