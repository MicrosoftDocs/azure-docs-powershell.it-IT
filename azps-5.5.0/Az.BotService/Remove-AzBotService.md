---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/remove-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
ms.openlocfilehash: ef75ec3e48a68bffce7c5b281f542bd2e3dba9d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195191"
---
# <span data-ttu-id="0076f-101">Remove-AzBotService</span><span class="sxs-lookup"><span data-stu-id="0076f-101">Remove-AzBotService</span></span>

## <span data-ttu-id="0076f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0076f-102">SYNOPSIS</span></span>
<span data-ttu-id="0076f-103">Elimina un servizio bot dal gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0076f-103">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="0076f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0076f-104">SYNTAX</span></span>

### <span data-ttu-id="0076f-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0076f-105">Delete (Default)</span></span>
```
Remove-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0076f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0076f-106">DeleteViaIdentity</span></span>
```
Remove-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0076f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0076f-107">DESCRIPTION</span></span>
<span data-ttu-id="0076f-108">Elimina un servizio bot dal gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0076f-108">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="0076f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0076f-109">EXAMPLES</span></span>

### <span data-ttu-id="0076f-110">Esempio 1: Eliminare BotService by Name e ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0076f-110">Example 1: Delete the BotService By Name and ResourceGroupName</span></span>
```powershell
PS C:\> Remove-AzBotService -Name youri-bot -ResourceGroupName youriBotTest

```

<span data-ttu-id="0076f-111">Eliminare BotService per nome e ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0076f-111">Delete the BotService By Name and ResourceGroupName</span></span>

### <span data-ttu-id="0076f-112">Esempio 2: Eliminare BotService per InputObject</span><span class="sxs-lookup"><span data-stu-id="0076f-112">Example 2: Delete the BotService By InputObject</span></span>
```powershell
PS C:\> $getservice = Get-AzBotService -Name youriechobottest -ResourceGroupName youriBotTest
Remove-AzBotService -InputObject $getservice

```

<span data-ttu-id="0076f-113">Eliminare BotService Per InputObject</span><span class="sxs-lookup"><span data-stu-id="0076f-113">Delete the BotService By InputObject</span></span>

## <span data-ttu-id="0076f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0076f-114">PARAMETERS</span></span>

### <span data-ttu-id="0076f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0076f-115">-DefaultProfile</span></span>
<span data-ttu-id="0076f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0076f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0076f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0076f-117">-InputObject</span></span>
<span data-ttu-id="0076f-118">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0076f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0076f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0076f-119">-Name</span></span>
<span data-ttu-id="0076f-120">Nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="0076f-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="0076f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0076f-121">-PassThru</span></span>
<span data-ttu-id="0076f-122">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="0076f-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0076f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0076f-123">-ResourceGroupName</span></span>
<span data-ttu-id="0076f-124">Nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0076f-124">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="0076f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0076f-125">-SubscriptionId</span></span>
<span data-ttu-id="0076f-126">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="0076f-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="0076f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0076f-127">-Confirm</span></span>
<span data-ttu-id="0076f-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0076f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0076f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0076f-129">-WhatIf</span></span>
<span data-ttu-id="0076f-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0076f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0076f-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0076f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0076f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0076f-132">CommonParameters</span></span>
<span data-ttu-id="0076f-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0076f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0076f-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0076f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0076f-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="0076f-135">INPUTS</span></span>

### <span data-ttu-id="0076f-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="0076f-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="0076f-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0076f-137">OUTPUTS</span></span>

### <span data-ttu-id="0076f-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0076f-138">System.Boolean</span></span>

## <span data-ttu-id="0076f-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="0076f-139">NOTES</span></span>

<span data-ttu-id="0076f-140">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0076f-140">ALIASES</span></span>

<span data-ttu-id="0076f-141">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="0076f-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0076f-142">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0076f-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0076f-143">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0076f-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0076f-144">INPUTOBJECT <IBotServiceIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="0076f-144">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0076f-145">`[ChannelName <ChannelName?>]`: nome della risorsa Canale.</span><span class="sxs-lookup"><span data-stu-id="0076f-145">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="0076f-146">`[ConnectionName <String>]`: nome della risorsa impostazione di connessione al servizio Bot</span><span class="sxs-lookup"><span data-stu-id="0076f-146">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="0076f-147">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="0076f-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0076f-148">`[ResourceGroupName <String>]`: nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0076f-148">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="0076f-149">`[ResourceName <String>]`: nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="0076f-149">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="0076f-150">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0076f-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="0076f-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0076f-151">RELATED LINKS</span></span>

