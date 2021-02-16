---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/remove-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Remove-AzADDomainService.md
ms.openlocfilehash: f29fbbdd805abb9891f707ed983bcf8aebefc46c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176590"
---
# <span data-ttu-id="a730c-101">Remove-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="a730c-101">Remove-AzADDomainService</span></span>

## <span data-ttu-id="a730c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a730c-102">SYNOPSIS</span></span>
<span data-ttu-id="a730c-103">L'operazione Elimina servizio di dominio elimina un servizio di dominio esistente.</span><span class="sxs-lookup"><span data-stu-id="a730c-103">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="a730c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a730c-104">SYNTAX</span></span>

### <span data-ttu-id="a730c-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a730c-105">Delete (Default)</span></span>
```
Remove-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a730c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a730c-106">DeleteViaIdentity</span></span>
```
Remove-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a730c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a730c-107">DESCRIPTION</span></span>
<span data-ttu-id="a730c-108">L'operazione Elimina servizio di dominio elimina un servizio di dominio esistente.</span><span class="sxs-lookup"><span data-stu-id="a730c-108">The Delete Domain Service operation deletes an existing Domain Service.</span></span>

## <span data-ttu-id="a730c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a730c-109">EXAMPLES</span></span>

### <span data-ttu-id="a730c-110">Esempio 1: Eliminare il dominio AzADDomain in base al nome e al nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a730c-110">Example 1: Delete the AzADDomain by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName

```

<span data-ttu-id="a730c-111">Eliminare il dominio AzADDomain in base al nome e al nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a730c-111">Delete the AzADDomain by ResourceGroupName and Name</span></span>

### <span data-ttu-id="a730c-112">Esempio 2: Eliminare AzADDomain per InputObject</span><span class="sxs-lookup"><span data-stu-id="a730c-112">Example 2: Delete the AzADDomain by InputObject</span></span>
```powershell
PS C:\> $GetADDomainExample = Get-AzADDomainService -ResourceGroupName $env.ResourceGroupName -Name $env.ADdomainName
Remove-AzADDomainService -InputObject $GetADDomainExample

```

<span data-ttu-id="a730c-113">Eliminare il dominio AzADDomain per InputObject</span><span class="sxs-lookup"><span data-stu-id="a730c-113">Delete the AzADDomain by InputObject</span></span>

## <span data-ttu-id="a730c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a730c-114">PARAMETERS</span></span>

### <span data-ttu-id="a730c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a730c-115">-AsJob</span></span>
<span data-ttu-id="a730c-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="a730c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="a730c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a730c-117">-DefaultProfile</span></span>
<span data-ttu-id="a730c-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a730c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a730c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a730c-119">-InputObject</span></span>
<span data-ttu-id="a730c-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a730c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a730c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a730c-121">-Name</span></span>
<span data-ttu-id="a730c-122">Nome del servizio di dominio.</span><span class="sxs-lookup"><span data-stu-id="a730c-122">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a730c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a730c-123">-NoWait</span></span>
<span data-ttu-id="a730c-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="a730c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a730c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a730c-125">-PassThru</span></span>
<span data-ttu-id="a730c-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="a730c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a730c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a730c-127">-ResourceGroupName</span></span>
<span data-ttu-id="a730c-128">Nome del gruppo di risorse nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a730c-128">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="a730c-129">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a730c-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a730c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a730c-130">-SubscriptionId</span></span>
<span data-ttu-id="a730c-131">Recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a730c-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a730c-132">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a730c-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a730c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a730c-133">-Confirm</span></span>
<span data-ttu-id="a730c-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a730c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a730c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a730c-135">-WhatIf</span></span>
<span data-ttu-id="a730c-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a730c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a730c-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a730c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a730c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a730c-138">CommonParameters</span></span>
<span data-ttu-id="a730c-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a730c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a730c-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a730c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a730c-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="a730c-141">INPUTS</span></span>

### <span data-ttu-id="a730c-142">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="a730c-142">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="a730c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a730c-143">OUTPUTS</span></span>

### <span data-ttu-id="a730c-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a730c-144">System.Boolean</span></span>

## <span data-ttu-id="a730c-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="a730c-145">NOTES</span></span>

<span data-ttu-id="a730c-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a730c-146">ALIASES</span></span>

<span data-ttu-id="a730c-147">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="a730c-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a730c-148">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a730c-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a730c-149">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a730c-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a730c-150">INPUTOBJECT <IAdDomainServicesIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="a730c-150">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a730c-151">`[DomainServiceName <String>]`: nome del servizio di dominio.</span><span class="sxs-lookup"><span data-stu-id="a730c-151">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="a730c-152">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="a730c-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a730c-153">`[ResourceGroupName <String>]`: nome del gruppo di risorse nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a730c-153">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="a730c-154">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="a730c-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="a730c-155">`[SubscriptionId <String>]`: recupera le credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a730c-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="a730c-156">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a730c-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a730c-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a730c-157">RELATED LINKS</span></span>

