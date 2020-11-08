---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 64639A35-0573-48C8-AB21-19FEB09537BA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b1b251a5fef3ad91f830e18714796421d2abca7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023716"
---
# <span data-ttu-id="b6a0b-101">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="b6a0b-101">Set-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="b6a0b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b6a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a0b-103">Associa un gruppo di sicurezza di rete a una macchina virtuale, un ruolo PaaS o una scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-103">Associates a network security group to a virtual machine, PaaS role, or network adapter.</span></span>

## <span data-ttu-id="b6a0b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6a0b-104">SYNTAX</span></span>

### <span data-ttu-id="b6a0b-105">AddNetworkSecurityGroupAssociationToSubnet</span><span class="sxs-lookup"><span data-stu-id="b6a0b-105">AddNetworkSecurityGroupAssociationToSubnet</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VirtualNetworkName <String>
 -SubnetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b6a0b-106">AddNetworkSecurityGroupAssociationToIaaSRole</span><span class="sxs-lookup"><span data-stu-id="b6a0b-106">AddNetworkSecurityGroupAssociationToIaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VM <PersistentVMRoleContext>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b6a0b-107">AddNetworkSecurityGroupAssociationToPaaSRole</span><span class="sxs-lookup"><span data-stu-id="b6a0b-107">AddNetworkSecurityGroupAssociationToPaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] [-Slot <String>]
 -RoleName <String> -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6a0b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6a0b-108">DESCRIPTION</span></span>
<span data-ttu-id="b6a0b-109">Il cmdlet **set-AzureNetworkSecurityGroupAssociation** associa un gruppo di sicurezza di rete a una macchina virtuale, a una piattaforma come a un ruolo di servizio (PaaS) o a una scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-109">The **Set-AzureNetworkSecurityGroupAssociation** cmdlet associates a network security group to a virtual machine, platform as a service (PaaS) role, or network adapter.</span></span>

## <span data-ttu-id="b6a0b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6a0b-110">EXAMPLES</span></span>

### <span data-ttu-id="b6a0b-111">Esempio 1: assegnare una macchina virtuale a un gruppo di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="b6a0b-111">Example 1: Assign a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="b6a0b-112">Questo comando ottiene una macchina virtuale denominata ContosoVM06 per il servizio denominato ContosoService e passa l'oggetto macchina virtuale al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="b6a0b-113">Il cmdlet corrente assegna il gruppo di sicurezza di rete denominato ContosoNetworkSecurityGroup alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-113">The current cmdlet assigns the network security group named ContosoNetworkSecurityGroup to that virtual machine.</span></span>

## <span data-ttu-id="b6a0b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b6a0b-114">PARAMETERS</span></span>

### <span data-ttu-id="b6a0b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b6a0b-115">-Force</span></span>
<span data-ttu-id="b6a0b-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b6a0b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6a0b-117">-Name</span></span>
<span data-ttu-id="b6a0b-118">Specifica il nome del gruppo di sicurezza di rete impostato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-118">Specifies the name of the network security group that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a0b-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="b6a0b-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="b6a0b-120">Specifica il nome della scheda di rete a cui questo cmdlet applica il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-120">Specifies the name of the network adapter to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a0b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6a0b-121">-PassThru</span></span>
<span data-ttu-id="b6a0b-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-122">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b6a0b-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b6a0b-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="b6a0b-124">-Profile</span></span>
<span data-ttu-id="b6a0b-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b6a0b-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6a0b-127">-RoleName</span><span class="sxs-lookup"><span data-stu-id="b6a0b-127">-RoleName</span></span>
<span data-ttu-id="b6a0b-128">Specifica il nome di un ruolo PaaS a cui questo cmdlet applica il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-128">Specifies the name of a PaaS role to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a0b-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b6a0b-129">-ServiceName</span></span>
<span data-ttu-id="b6a0b-130">Specifica il nome di un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="b6a0b-131">Il ruolo PaaS appartiene al servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-131">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a0b-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="b6a0b-132">-Slot</span></span>
<span data-ttu-id="b6a0b-133">Specifica uno slot PaaS.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="b6a0b-134">Il ruolo PaaS per cui questo cmdlet imposta il gruppo di sicurezza di rete ha lo slot specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-134">The PaaS role for which this cmdlet sets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="b6a0b-135">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="b6a0b-135">Valid values are:</span></span> 

- <span data-ttu-id="b6a0b-136">Produzione</span><span class="sxs-lookup"><span data-stu-id="b6a0b-136">Production</span></span>
- <span data-ttu-id="b6a0b-137">Gestione temporanea</span><span class="sxs-lookup"><span data-stu-id="b6a0b-137">Staging</span></span> 

<span data-ttu-id="b6a0b-138">Il valore predefinito è Production.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a0b-139">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b6a0b-139">-SubnetName</span></span>
<span data-ttu-id="b6a0b-140">Specifica il nome di una subnet a cui questo cmdlet associa il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-140">Specifies the name of a subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a0b-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b6a0b-141">-VirtualNetworkName</span></span>
<span data-ttu-id="b6a0b-142">Specifica il nome di una rete virtuale che contiene la subnet a cui questo cmdlet associa il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-142">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a0b-143">-VM</span><span class="sxs-lookup"><span data-stu-id="b6a0b-143">-VM</span></span>
<span data-ttu-id="b6a0b-144">Specifica la macchina virtuale a cui questo cmdlet applica il gruppo di sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a0b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a0b-145">CommonParameters</span></span>
<span data-ttu-id="b6a0b-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a0b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a0b-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a0b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a0b-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b6a0b-148">INPUTS</span></span>

## <span data-ttu-id="b6a0b-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6a0b-149">OUTPUTS</span></span>

### <span data-ttu-id="b6a0b-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6a0b-150">System.Boolean</span></span>

## <span data-ttu-id="b6a0b-151">Note</span><span class="sxs-lookup"><span data-stu-id="b6a0b-151">NOTES</span></span>

## <span data-ttu-id="b6a0b-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6a0b-152">RELATED LINKS</span></span>

[<span data-ttu-id="b6a0b-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="b6a0b-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="b6a0b-154">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="b6a0b-154">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)


