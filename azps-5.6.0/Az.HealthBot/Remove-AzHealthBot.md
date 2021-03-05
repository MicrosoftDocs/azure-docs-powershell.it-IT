---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/remove-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
ms.openlocfilehash: 2b2a4eba0a062b90866479409e80bbe7e55c1984
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013214"
---
# <span data-ttu-id="f6b2c-101">Remove-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="f6b2c-101">Remove-AzHealthBot</span></span>

## <span data-ttu-id="f6b2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6b2c-102">SYNOPSIS</span></span>
<span data-ttu-id="f6b2c-103">Eliminare un modello HealthBot.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-103">Delete a HealthBot.</span></span>

## <span data-ttu-id="f6b2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6b2c-104">SYNTAX</span></span>

### <span data-ttu-id="f6b2c-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f6b2c-105">Delete (Default)</span></span>
```
Remove-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f6b2c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f6b2c-106">DeleteViaIdentity</span></span>
```
Remove-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f6b2c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f6b2c-107">DESCRIPTION</span></span>
<span data-ttu-id="f6b2c-108">Eliminare un modello HealthBot.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-108">Delete a HealthBot.</span></span>

## <span data-ttu-id="f6b2c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6b2c-109">EXAMPLES</span></span>

### <span data-ttu-id="f6b2c-110">Esempio 1: Eliminare HealthBot in base al nome e al nome ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6b2c-110">Example 1: Delete HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzHealthBot -Name yourihealthbot -ResourceGroupName youriTest

```

<span data-ttu-id="f6b2c-111">Eliminare HealthBot per NomeGruppo ResourceGroup e Nome</span><span class="sxs-lookup"><span data-stu-id="f6b2c-111">Delete HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="f6b2c-112">Esempio 2: Eliminare HealthBot per InputObject</span><span class="sxs-lookup"><span data-stu-id="f6b2c-112">Example 2: Delete HealthBot by InputObject</span></span>
```powershell
PS C:\> $gethealthbot = Get-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest
Remove-AzHealthBot -InputObject $gethealthbot

```

<span data-ttu-id="f6b2c-113">Eliminare HealthBot per InputObject</span><span class="sxs-lookup"><span data-stu-id="f6b2c-113">Delete HealthBot by InputObject</span></span>

## <span data-ttu-id="f6b2c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6b2c-114">PARAMETERS</span></span>

### <span data-ttu-id="f6b2c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6b2c-115">-AsJob</span></span>
<span data-ttu-id="f6b2c-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="f6b2c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f6b2c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6b2c-117">-DefaultProfile</span></span>
<span data-ttu-id="f6b2c-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b2c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6b2c-119">-InputObject</span></span>
<span data-ttu-id="f6b2c-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b2c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f6b2c-121">-Name</span></span>
<span data-ttu-id="f6b2c-122">Nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-122">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b2c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f6b2c-123">-NoWait</span></span>
<span data-ttu-id="f6b2c-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="f6b2c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f6b2c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6b2c-125">-PassThru</span></span>
<span data-ttu-id="f6b2c-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="f6b2c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f6b2c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6b2c-127">-ResourceGroupName</span></span>
<span data-ttu-id="f6b2c-128">Nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-128">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b2c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6b2c-129">-SubscriptionId</span></span>
<span data-ttu-id="f6b2c-130">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b2c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6b2c-131">-Confirm</span></span>
<span data-ttu-id="f6b2c-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6b2c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6b2c-133">-WhatIf</span></span>
<span data-ttu-id="f6b2c-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6b2c-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6b2c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6b2c-136">CommonParameters</span></span>
<span data-ttu-id="f6b2c-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6b2c-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6b2c-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="f6b2c-139">INPUTS</span></span>

### <span data-ttu-id="f6b2c-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="f6b2c-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="f6b2c-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6b2c-141">OUTPUTS</span></span>

### <span data-ttu-id="f6b2c-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f6b2c-142">System.Boolean</span></span>

## <span data-ttu-id="f6b2c-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="f6b2c-143">NOTES</span></span>

<span data-ttu-id="f6b2c-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f6b2c-144">ALIASES</span></span>

<span data-ttu-id="f6b2c-145">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="f6b2c-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f6b2c-146">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6b2c-147">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f6b2c-148">INPUTOBJECT <IHealthBotIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f6b2c-148">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6b2c-149">`[BotName <String>]`: nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-149">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="f6b2c-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="f6b2c-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6b2c-151">`[ResourceGroupName <String>]`: nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-151">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="f6b2c-152">`[SubscriptionId <String>]`: ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="f6b2c-152">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="f6b2c-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6b2c-153">RELATED LINKS</span></span>

