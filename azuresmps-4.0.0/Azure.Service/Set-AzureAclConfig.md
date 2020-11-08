---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A9E43722-DEE2-4A5C-A3F6-8DA6612735AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34e6e98c2bf506e8102287251e18dceda4dd0c7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029894"
---
# <span data-ttu-id="b84bf-101">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="b84bf-101">Set-AzureAclConfig</span></span>

## <span data-ttu-id="b84bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b84bf-102">SYNOPSIS</span></span>
<span data-ttu-id="b84bf-103">Modifica un oggetto di configurazione ACL.</span><span class="sxs-lookup"><span data-stu-id="b84bf-103">Modifies an ACL configuration object.</span></span>

## <span data-ttu-id="b84bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b84bf-104">SYNTAX</span></span>

### <span data-ttu-id="b84bf-105">AddRule</span><span class="sxs-lookup"><span data-stu-id="b84bf-105">AddRule</span></span>
```
Set-AzureAclConfig [-AddRule] [-Action] <String> [-RemoteSubnet] <String> [[-Order] <Int32>]
 [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b84bf-106">RemoveRule</span><span class="sxs-lookup"><span data-stu-id="b84bf-106">RemoveRule</span></span>
```
Set-AzureAclConfig [-RemoveRule] [-RuleId] <Int32> -ACL <NetworkAclObject>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b84bf-107">Regola</span><span class="sxs-lookup"><span data-stu-id="b84bf-107">SetRule</span></span>
```
Set-AzureAclConfig [-SetRule] [-RuleId] <Int32> [[-Action] <String>] [[-RemoteSubnet] <String>]
 [[-Order] <Int32>] [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b84bf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b84bf-108">DESCRIPTION</span></span>
<span data-ttu-id="b84bf-109">Il cmdlet **set-AzureAclConfig** modifica un oggetto di configurazione dell'elenco di controllo di Access (ACL) da una configurazione di una macchina virtuale Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="b84bf-109">The **Set-AzureAclConfig** cmdlet modifies an access control list (ACL) configuration object from an existing Azure virtual machine configuration.</span></span>

## <span data-ttu-id="b84bf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b84bf-110">EXAMPLES</span></span>

### <span data-ttu-id="b84bf-111">Esempio 1: aggiungere una regola a una nuova configurazione ACL</span><span class="sxs-lookup"><span data-stu-id="b84bf-111">Example 1: Add a rule to a new ACL configuration</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
PS C:\> Set-AzureAclConfig -AddRule -ACL $Acl -Action Permit -RemoteSubnet "172.0.0.0/8" -Order 100 -Description "Permit ACL rule"
```

<span data-ttu-id="b84bf-112">Il primo comando crea una configurazione ACL e la archivia nella variabile $Acl.</span><span class="sxs-lookup"><span data-stu-id="b84bf-112">The first command creates an ACL configuration, and then stores it in the $Acl variable.</span></span>

<span data-ttu-id="b84bf-113">Il secondo comando aggiunge una nuova regola alla configurazione archiviata in $Acl.</span><span class="sxs-lookup"><span data-stu-id="b84bf-113">The second command adds a new rule to the configuration stored in $Acl.</span></span>
<span data-ttu-id="b84bf-114">Il comando specifica un'azione, una subnet, un ordine e una descrizione per la regola.</span><span class="sxs-lookup"><span data-stu-id="b84bf-114">The command specifies an action, subnet, order, and description for the rule.</span></span>

### <span data-ttu-id="b84bf-115">Esempio 2: modificare una regola in una configurazione ACL</span><span class="sxs-lookup"><span data-stu-id="b84bf-115">Example 2: Modify a rule in an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -SetRule -RuleId 0 -ACL $Acl -Order 102 -Description "Web endpoint rule"
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="b84bf-116">Il primo comando ottiene la macchina virtuale denominata VirtualMachine07 nel servizio denominato ContosoService usando il cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="b84bf-116">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="b84bf-117">Il comando passa l'oggetto al cmdlet **Get-AzureAclConfig** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="b84bf-117">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b84bf-118">Questo cmdlet ottiene la configurazione ACL per l'endpoint denominato Web.</span><span class="sxs-lookup"><span data-stu-id="b84bf-118">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="b84bf-119">Il comando Archivia l'oggetto di configurazione ACL nella variabile $Acl.</span><span class="sxs-lookup"><span data-stu-id="b84bf-119">The command stores that ACL configuration object in the $Acl variable.</span></span>

<span data-ttu-id="b84bf-120">Il secondo comando modifica la regola con l'ID 0.</span><span class="sxs-lookup"><span data-stu-id="b84bf-120">The second command modifies the rule that has the ID of 0.</span></span>
<span data-ttu-id="b84bf-121">Il comando modifica l'ordine e la descrizione della regola.</span><span class="sxs-lookup"><span data-stu-id="b84bf-121">The command changes the order and the description of the rule.</span></span>

<span data-ttu-id="b84bf-122">Il comando Final imposta l'oggetto di configurazione ACL per la macchina virtuale usando il cmdlet **set-AzureEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="b84bf-122">The final command sets the ACL configuration object for that virtual machine by using the **Set-AzureEndpoint** cmdlet.</span></span>
<span data-ttu-id="b84bf-123">Il comando Aggiorna anche la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b84bf-123">The command also updates that virtual machine.</span></span>

### <span data-ttu-id="b84bf-124">Esempio 3: rimuovere una regola da una configurazione ACL</span><span class="sxs-lookup"><span data-stu-id="b84bf-124">Example 3: Remove a rule from an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -RemoveRule -ID 0 -ACL $Acl
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="b84bf-125">Il primo comando Archivia un oggetto di configurazione ACL nella variabile $Acl.</span><span class="sxs-lookup"><span data-stu-id="b84bf-125">The first command stores an ACL configuration object in the $Acl variable.</span></span>
<span data-ttu-id="b84bf-126">Questo è lo stesso dell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="b84bf-126">This is the same as the previous example.</span></span>

<span data-ttu-id="b84bf-127">Il secondo comando rimuove la regola che contiene l'ID 0 dalla configurazione ACL in $Acl.</span><span class="sxs-lookup"><span data-stu-id="b84bf-127">The second command removes the rule that has the ID 0 from the ACL configuration in $Acl.</span></span>

<span data-ttu-id="b84bf-128">Il comando Final imposta l'oggetto di configurazione ACL per la macchina virtuale e aggiorna la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b84bf-128">The final command sets the ACL configuration object for the virtual machine and updates that virtual machine.</span></span>
<span data-ttu-id="b84bf-129">Questo è lo stesso dell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="b84bf-129">This is the same as the previous example.</span></span>

## <span data-ttu-id="b84bf-130">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b84bf-130">PARAMETERS</span></span>

### <span data-ttu-id="b84bf-131">-ACL</span><span class="sxs-lookup"><span data-stu-id="b84bf-131">-ACL</span></span>
<span data-ttu-id="b84bf-132">Specifica un oggetto di configurazione ACL modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b84bf-132">Specifies an ACL configuration object that this cmdlet modifies.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b84bf-133">-Azione</span><span class="sxs-lookup"><span data-stu-id="b84bf-133">-Action</span></span>
<span data-ttu-id="b84bf-134">Specifica l'azione per la regola aggiunta o modifica di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b84bf-134">Specifies the action for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="b84bf-135">I valori validi sono: permesso e negazione.</span><span class="sxs-lookup"><span data-stu-id="b84bf-135">Valid values are: Permit and Deny.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84bf-136">-AddRule</span><span class="sxs-lookup"><span data-stu-id="b84bf-136">-AddRule</span></span>
<span data-ttu-id="b84bf-137">Indica che questo cmdlet aggiunge una regola alla configurazione ACL.</span><span class="sxs-lookup"><span data-stu-id="b84bf-137">Indicates that this cmdlet adds a rule to the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AddRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84bf-138">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="b84bf-138">-Description</span></span>
<span data-ttu-id="b84bf-139">Specifica una descrizione per la regola aggiunta o modifica di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b84bf-139">Specifies a description for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: String
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84bf-140">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b84bf-140">-InformationAction</span></span>
<span data-ttu-id="b84bf-141">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="b84bf-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b84bf-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b84bf-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b84bf-143">Continuare</span><span class="sxs-lookup"><span data-stu-id="b84bf-143">Continue</span></span>
- <span data-ttu-id="b84bf-144">Ignora</span><span class="sxs-lookup"><span data-stu-id="b84bf-144">Ignore</span></span>
- <span data-ttu-id="b84bf-145">Informarsi</span><span class="sxs-lookup"><span data-stu-id="b84bf-145">Inquire</span></span>
- <span data-ttu-id="b84bf-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b84bf-146">SilentlyContinue</span></span>
- <span data-ttu-id="b84bf-147">Stop</span><span class="sxs-lookup"><span data-stu-id="b84bf-147">Stop</span></span>
- <span data-ttu-id="b84bf-148">Sospensione</span><span class="sxs-lookup"><span data-stu-id="b84bf-148">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84bf-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b84bf-149">-InformationVariable</span></span>
<span data-ttu-id="b84bf-150">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="b84bf-150">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84bf-151">-Ordine</span><span class="sxs-lookup"><span data-stu-id="b84bf-151">-Order</span></span>
<span data-ttu-id="b84bf-152">Specifica l'ordine di elaborazione per la regola aggiunta o modifica di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b84bf-152">Specifies the processing order for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84bf-153">-RemoteSubnet</span><span class="sxs-lookup"><span data-stu-id="b84bf-153">-RemoteSubnet</span></span>
<span data-ttu-id="b84bf-154">Specifica la subnet remota per la regola aggiunta o modifica di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b84bf-154">Specifies the remote subnet for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="b84bf-155">Specifica un indirizzo in formato CIDR (classe Interdomain Routing).</span><span class="sxs-lookup"><span data-stu-id="b84bf-155">Specifies an address in Classless Interdomain Routing (CIDR) format.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84bf-156">-RemoveRule</span><span class="sxs-lookup"><span data-stu-id="b84bf-156">-RemoveRule</span></span>
<span data-ttu-id="b84bf-157">Indica che questo cmdlet rimuove una regola dalla configurazione ACL.</span><span class="sxs-lookup"><span data-stu-id="b84bf-157">Indicates that this cmdlet removes a rule from the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84bf-158">-RuleId</span><span class="sxs-lookup"><span data-stu-id="b84bf-158">-RuleId</span></span>
<span data-ttu-id="b84bf-159">Specifica l'ID della regola che questo cmdlet rimuove o modifica per la configurazione dell'ACL.</span><span class="sxs-lookup"><span data-stu-id="b84bf-159">Specifies the ID of the rule that this cmdlet removes or modifies for the ACL configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveRule, SetRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84bf-160">-Serule</span><span class="sxs-lookup"><span data-stu-id="b84bf-160">-SetRule</span></span>
<span data-ttu-id="b84bf-161">Indica che questo cmdlet modifica una regola nella configurazione ACL.</span><span class="sxs-lookup"><span data-stu-id="b84bf-161">Indicates that this cmdlet modifies a rule in the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b84bf-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b84bf-162">CommonParameters</span></span>
<span data-ttu-id="b84bf-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b84bf-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b84bf-164">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b84bf-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b84bf-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b84bf-165">INPUTS</span></span>

## <span data-ttu-id="b84bf-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b84bf-166">OUTPUTS</span></span>

## <span data-ttu-id="b84bf-167">Note</span><span class="sxs-lookup"><span data-stu-id="b84bf-167">NOTES</span></span>

## <span data-ttu-id="b84bf-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b84bf-168">RELATED LINKS</span></span>

[<span data-ttu-id="b84bf-169">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="b84bf-169">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="b84bf-170">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b84bf-170">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="b84bf-171">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="b84bf-171">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="b84bf-172">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="b84bf-172">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="b84bf-173">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="b84bf-173">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="b84bf-174">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b84bf-174">Update-AzureVM</span></span>](./Update-AzureVM.md)


