---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: AA9686AF-2D03-43DB-A91B-50D06D674A3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8da83231a16f4c846f09d03374d6e35757e1ba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023914"
---
# <span data-ttu-id="3eccd-101">Set-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="3eccd-101">Set-AzureIPForwarding</span></span>

## <span data-ttu-id="3eccd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3eccd-102">SYNOPSIS</span></span>
<span data-ttu-id="3eccd-103">Abilita o Disabilita l'inoltro IP.</span><span class="sxs-lookup"><span data-stu-id="3eccd-103">Enables or disables IP forwarding.</span></span>

## <span data-ttu-id="3eccd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3eccd-104">SYNTAX</span></span>

### <span data-ttu-id="3eccd-105">EnableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="3eccd-105">EnableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3eccd-106">DisableIaaSIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="3eccd-106">DisableIaaSIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -VM <PersistentVMRoleContext> -ServiceName <String> [-NetworkInterfaceName <String>]
 [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3eccd-107">EnableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="3eccd-107">EnableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Enable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3eccd-108">DisableSlotIPForwardingParamSet</span><span class="sxs-lookup"><span data-stu-id="3eccd-108">DisableSlotIPForwardingParamSet</span></span>
```
Set-AzureIPForwarding -ServiceName <String> [-Slot <String>] -RoleName <String>
 [-NetworkInterfaceName <String>] [-Disable] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3eccd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3eccd-109">DESCRIPTION</span></span>
<span data-ttu-id="3eccd-110">Il cmdlet **set-AzureIPForwarding** Abilita o Disabilita l'inoltro IP per una macchina virtuale, per un ruolo Platform as a Service (PaaS) o una scheda di rete che appartiene a una macchina virtuale o a un ruolo PaaS.</span><span class="sxs-lookup"><span data-stu-id="3eccd-110">The **Set-AzureIPForwarding** cmdlet enables or disables IP forwarding for a virtual machine, for a platform as a service (PaaS) role, or a network adapter that belongs to a virtual machine or PaaS role.</span></span>

## <span data-ttu-id="3eccd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3eccd-111">EXAMPLES</span></span>

### <span data-ttu-id="3eccd-112">Esempio 1: abilitare l'inoltro IP per una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="3eccd-112">Example 1: Enable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Enable
```

<span data-ttu-id="3eccd-113">Questo comando ottiene una macchina virtuale denominata ContosoVM06 per il servizio denominato ContosoService e passa l'oggetto macchina virtuale al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="3eccd-113">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="3eccd-114">Il cmdlet corrente consente l'inoltro IP per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3eccd-114">The current cmdlet enables IP forwarding for that virtual machine.</span></span>

### <span data-ttu-id="3eccd-115">Esempio 2: disabilitare l'inoltro IP per una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="3eccd-115">Example 2: Disable IP forwarding for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureIPForwarding -Disable
```

<span data-ttu-id="3eccd-116">Questo comando ottiene una macchina virtuale denominata ContosoVM06 per il servizio denominato ContosoService e passa l'oggetto macchina virtuale al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="3eccd-116">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="3eccd-117">Il cmdlet corrente Disabilita l'inoltro IP per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3eccd-117">The current cmdlet disables IP forwarding for that virtual machine.</span></span>

## <span data-ttu-id="3eccd-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3eccd-118">PARAMETERS</span></span>

### <span data-ttu-id="3eccd-119">-Disable</span><span class="sxs-lookup"><span data-stu-id="3eccd-119">-Disable</span></span>
<span data-ttu-id="3eccd-120">Indica che questo cmdlet disabilita l'inoltro IP.</span><span class="sxs-lookup"><span data-stu-id="3eccd-120">Indicates that this cmdlet disables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableIaaSIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eccd-121">-Enable</span><span class="sxs-lookup"><span data-stu-id="3eccd-121">-Enable</span></span>
<span data-ttu-id="3eccd-122">Indica che questo cmdlet Abilita l'inoltro IP.</span><span class="sxs-lookup"><span data-stu-id="3eccd-122">Indicates that this cmdlet enables IP forwarding.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableIaaSIPForwardingParamSet, EnableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eccd-123">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="3eccd-123">-NetworkInterfaceName</span></span>
<span data-ttu-id="3eccd-124">Specifica il nome della scheda di rete in cui questo cmdlet imposta l'inoltro IP.</span><span class="sxs-lookup"><span data-stu-id="3eccd-124">Specifies the name of the network adapter on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eccd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3eccd-125">-PassThru</span></span>
<span data-ttu-id="3eccd-126">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="3eccd-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3eccd-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="3eccd-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3eccd-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="3eccd-128">-Profile</span></span>
<span data-ttu-id="3eccd-129">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3eccd-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3eccd-130">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3eccd-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3eccd-131">-RoleName</span><span class="sxs-lookup"><span data-stu-id="3eccd-131">-RoleName</span></span>
<span data-ttu-id="3eccd-132">Specifica il nome di un ruolo PaaS in cui questo cmdlet imposta l'inoltro IP.</span><span class="sxs-lookup"><span data-stu-id="3eccd-132">Specifies the name of a PaaS role on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eccd-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3eccd-133">-ServiceName</span></span>
<span data-ttu-id="3eccd-134">Specifica il nome di un servizio cloud.</span><span class="sxs-lookup"><span data-stu-id="3eccd-134">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="3eccd-135">Il ruolo PaaS appartiene al servizio specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3eccd-135">The PaaS role belongs to the service that this parameter specifies.</span></span>

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

### <span data-ttu-id="3eccd-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="3eccd-136">-Slot</span></span>
<span data-ttu-id="3eccd-137">Specifica uno slot PaaS.</span><span class="sxs-lookup"><span data-stu-id="3eccd-137">Specifies a PaaS slot.</span></span>
<span data-ttu-id="3eccd-138">Il ruolo PaaS per cui questo cmdlet imposta l'inoltro ha lo slot specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3eccd-138">The PaaS role for which this cmdlet sets forwarding has the slot that this parameter specifies.</span></span>
<span data-ttu-id="3eccd-139">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="3eccd-139">Valid values are:</span></span>

- <span data-ttu-id="3eccd-140">Produzione</span><span class="sxs-lookup"><span data-stu-id="3eccd-140">Production</span></span>
- <span data-ttu-id="3eccd-141">Gestione temporanea</span><span class="sxs-lookup"><span data-stu-id="3eccd-141">Staging</span></span>

<span data-ttu-id="3eccd-142">Il valore predefinito è Production.</span><span class="sxs-lookup"><span data-stu-id="3eccd-142">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: EnableSlotIPForwardingParamSet, DisableSlotIPForwardingParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eccd-143">-VM</span><span class="sxs-lookup"><span data-stu-id="3eccd-143">-VM</span></span>
<span data-ttu-id="3eccd-144">Specifica l'oggetto macchina virtuale in cui questo cmdlet imposta l'inoltro IP.</span><span class="sxs-lookup"><span data-stu-id="3eccd-144">Specifies the virtual machine object on which this cmdlet sets IP forwarding.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: EnableIaaSIPForwardingParamSet, DisableIaaSIPForwardingParamSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3eccd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eccd-145">CommonParameters</span></span>
<span data-ttu-id="3eccd-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eccd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eccd-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eccd-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eccd-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3eccd-148">INPUTS</span></span>

## <span data-ttu-id="3eccd-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3eccd-149">OUTPUTS</span></span>

### <span data-ttu-id="3eccd-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3eccd-150">System.Boolean</span></span>

## <span data-ttu-id="3eccd-151">Note</span><span class="sxs-lookup"><span data-stu-id="3eccd-151">NOTES</span></span>

## <span data-ttu-id="3eccd-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3eccd-152">RELATED LINKS</span></span>

[<span data-ttu-id="3eccd-153">Get-AzureIPForwarding</span><span class="sxs-lookup"><span data-stu-id="3eccd-153">Get-AzureIPForwarding</span></span>](./Get-AzureIPForwarding.md)
