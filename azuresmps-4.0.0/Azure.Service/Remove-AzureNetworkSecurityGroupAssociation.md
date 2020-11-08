---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E3E0237-8E2D-4B3A-AD0C-2121DDE1AAB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28259b97f382092f5e6293048c040688011cfe92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029614"
---
# <span data-ttu-id="d5bb8-101">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="d5bb8-101">Remove-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="d5bb8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d5bb8-102">SYNOPSIS</span></span>
<span data-ttu-id="d5bb8-103">Rimuove un gruppo di sicurezza di rete.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-103">Removes a network security group.</span></span>

## <span data-ttu-id="d5bb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5bb8-104">SYNTAX</span></span>

### <span data-ttu-id="d5bb8-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span><span class="sxs-lookup"><span data-stu-id="d5bb8-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d5bb8-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span><span class="sxs-lookup"><span data-stu-id="d5bb8-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d5bb8-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span><span class="sxs-lookup"><span data-stu-id="d5bb8-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> [-Slot <String>] -RoleName <String>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5bb8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5bb8-108">DESCRIPTION</span></span>
<span data-ttu-id="d5bb8-109">Il cmdlet **Remove-AzureNetworkSecurityGroupAssociation** rimuove un gruppo di sicurezza di rete da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-109">The **Remove-AzureNetworkSecurityGroupAssociation** cmdlet removes a network security group from a virtual machine.</span></span>

## <span data-ttu-id="d5bb8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5bb8-110">EXAMPLES</span></span>

### <span data-ttu-id="d5bb8-111">Esempio 1: rimuovere una macchina virtuale in un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="d5bb8-111">Example 1: Remove a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Remove-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="d5bb8-112">Questo comando ottiene una macchina virtuale denominata ContosoVM06 per il servizio denominato ContosoService e passa l'oggetto macchina virtuale al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="d5bb8-113">Il cmdlet corrente rimuove il gruppo di sicurezza di rete denominato ContosoNetworkSecurityGroup da tale macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-113">The current cmdlet removes the network security group named ContosoNetworkSecurityGroup from that virtual machine.</span></span>

## <span data-ttu-id="d5bb8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d5bb8-114">PARAMETERS</span></span>

### <span data-ttu-id="d5bb8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d5bb8-115">-Force</span></span>
<span data-ttu-id="d5bb8-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d5bb8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5bb8-117">-Name</span></span>
<span data-ttu-id="d5bb8-118">Specifica il nome del gruppo di sicurezza di rete rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d5bb8-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="d5bb8-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="d5bb8-120">Specifica il nome della scheda di rete da cui questo cmdlet rimuove il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-120">Specifies the name of the network adapter from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5bb8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5bb8-121">-PassThru</span></span>
<span data-ttu-id="d5bb8-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d5bb8-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d5bb8-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="d5bb8-124">-Profile</span></span>
<span data-ttu-id="d5bb8-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d5bb8-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d5bb8-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="d5bb8-127">-RoleName</span></span>
<span data-ttu-id="d5bb8-128">Specifica il nome di un ruolo PaaS da cui questo cmdlet rimuove il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-128">Specifies the name of a PaaS role from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5bb8-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d5bb8-129">-ServiceName</span></span>
<span data-ttu-id="d5bb8-130">Specifica il nome di un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="d5bb8-131">Il ruolo PaaS da cui questo cmdlet rimuove un gruppo di sicurezza di rete appartiene al servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-131">The PaaS role from which this cmdlet removes a network security group belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5bb8-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="d5bb8-132">-Slot</span></span>
<span data-ttu-id="d5bb8-133">Specifica uno slot PaaS.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="d5bb8-134">Il ruolo PaaS da cui questo cmdlet rimuove un gruppo di sicurezza di rete ha lo slot specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-134">The PaaS role from which this cmdlet removes a network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="d5bb8-135">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="d5bb8-135">Valid values are:</span></span>

- <span data-ttu-id="d5bb8-136">Produzione</span><span class="sxs-lookup"><span data-stu-id="d5bb8-136">Production</span></span>
- <span data-ttu-id="d5bb8-137">Gestione temporanea</span><span class="sxs-lookup"><span data-stu-id="d5bb8-137">Staging</span></span>

<span data-ttu-id="d5bb8-138">Il valore predefinito è Production.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5bb8-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="d5bb8-139">-SubnetName</span></span>
<span data-ttu-id="d5bb8-140">Specifica il nome di una subnet da cui questo cmdlet rimuove il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-140">Specifies the name of a subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5bb8-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d5bb8-141">-VirtualNetworkName</span></span>
<span data-ttu-id="d5bb8-142">Specifica il nome di una rete virtuale che contiene la subnet da cui questo cmdlet rimuove il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-142">Specifies the name of a virtual network that contains the subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5bb8-143">-VM</span><span class="sxs-lookup"><span data-stu-id="d5bb8-143">-VM</span></span>
<span data-ttu-id="d5bb8-144">Specifica la macchina virtuale a cui questo cmdlet applica il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5bb8-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5bb8-145">CommonParameters</span></span>
<span data-ttu-id="d5bb8-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5bb8-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5bb8-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5bb8-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5bb8-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d5bb8-148">INPUTS</span></span>

## <span data-ttu-id="d5bb8-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5bb8-149">OUTPUTS</span></span>

### <span data-ttu-id="d5bb8-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d5bb8-150">System.Boolean</span></span>

## <span data-ttu-id="d5bb8-151">Note</span><span class="sxs-lookup"><span data-stu-id="d5bb8-151">NOTES</span></span>

## <span data-ttu-id="d5bb8-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5bb8-152">RELATED LINKS</span></span>

[<span data-ttu-id="d5bb8-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="d5bb8-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="d5bb8-154">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="d5bb8-154">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)
