---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
ms.openlocfilehash: b97b0d640b00e2aa3b75d829464f8ebe7dd4f6d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177798"
---
# <span data-ttu-id="0976c-101">New-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="0976c-101">New-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="0976c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0976c-102">SYNOPSIS</span></span>
<span data-ttu-id="0976c-103">Rigenerare la chiave di accesso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="0976c-103">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="0976c-104">Non è possibile rigenerare contemporaneamente PrimaryKey e SecondaryKey.</span><span class="sxs-lookup"><span data-stu-id="0976c-104">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="0976c-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0976c-105">SYNTAX</span></span>

### <span data-ttu-id="0976c-106">RegenerateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0976c-106">RegenerateExpanded (Default)</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyType <KeyType>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0976c-107">Rigenerare</span><span class="sxs-lookup"><span data-stu-id="0976c-107">Regenerate</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 -Parameter <IRegenerateKeyParameters> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0976c-108">RigenerareViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0976c-108">RegenerateViaIdentity</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> -Parameter <IRegenerateKeyParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0976c-109">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0976c-109">RegenerateViaIdentityExpanded</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> [-KeyType <KeyType>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0976c-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0976c-110">DESCRIPTION</span></span>
<span data-ttu-id="0976c-111">Rigenerare la chiave di accesso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="0976c-111">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="0976c-112">Non è possibile rigenerare contemporaneamente PrimaryKey e SecondaryKey.</span><span class="sxs-lookup"><span data-stu-id="0976c-112">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="0976c-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0976c-113">EXAMPLES</span></span>

### <span data-ttu-id="0976c-114">Esempio 1: Rigenerare la chiave primaria usando una tabella hash IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="0976c-114">Example 1: Regenerates the Primary key using a IRegenerateKeyParameters hashtable</span></span>
```powershell
PS > New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Parameter @{KeyType="Primary"}

PrimaryConnectionString              PrimaryKey
-----------------------              ----------
endpoint=<example-primary-endpoint>  <example-primarykey>
```

<span data-ttu-id="0976c-115">Invalida la chiave primaria precedente, rigenera una nuova chiave e la restituisce.</span><span class="sxs-lookup"><span data-stu-id="0976c-115">Invalidates the previous Primary key, regenerate a new one and return it.</span></span>

### <span data-ttu-id="0976c-116">Esempio 2: Rigenera la chiave secondaria con keyType</span><span class="sxs-lookup"><span data-stu-id="0976c-116">Example 2: Regenerates the Secondary key using a KeyType</span></span>
```powershell
PS C:\> New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -KeyType Secondary

SecondaryConnectionString               SecondaryKey
-----------------------                 ----------
endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="0976c-117">Invalida la chiave secondaria precedente, rigenera una nuova chiave e la restituisce.</span><span class="sxs-lookup"><span data-stu-id="0976c-117">Invalidates the previous Secondary key, regenerate a new one and return it.</span></span>

## <span data-ttu-id="0976c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0976c-118">PARAMETERS</span></span>

### <span data-ttu-id="0976c-119">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="0976c-119">-CommunicationServiceName</span></span>
<span data-ttu-id="0976c-120">Nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="0976c-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0976c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0976c-121">-DefaultProfile</span></span>
<span data-ttu-id="0976c-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0976c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0976c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0976c-123">-InputObject</span></span>
<span data-ttu-id="0976c-124">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0976c-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: RegenerateViaIdentity, RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0976c-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="0976c-125">-KeyType</span></span>
<span data-ttu-id="0976c-126">KeyType da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="0976c-126">The keyType to regenerate.</span></span>
<span data-ttu-id="0976c-127">Deve essere "principale" o "secondario" (senza distinzione tra maiuscole e minuscole).</span><span class="sxs-lookup"><span data-stu-id="0976c-127">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Support.KeyType
Parameter Sets: RegenerateExpanded, RegenerateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0976c-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="0976c-128">-Parameter</span></span>
<span data-ttu-id="0976c-129">Parameters descrive la richiesta di rigenerare le chiavi di accesso Da creare, vedere la sezione NOTE per le proprietà PARAMETER e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0976c-129">Parameters describes the request to regenerate access keys To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters
Parameter Sets: Regenerate, RegenerateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0976c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0976c-130">-ResourceGroupName</span></span>
<span data-ttu-id="0976c-131">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0976c-131">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0976c-132">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="0976c-132">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0976c-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0976c-133">-SubscriptionId</span></span>
<span data-ttu-id="0976c-134">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0976c-134">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0976c-135">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="0976c-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0976c-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0976c-136">-Confirm</span></span>
<span data-ttu-id="0976c-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0976c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0976c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0976c-138">-WhatIf</span></span>
<span data-ttu-id="0976c-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0976c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0976c-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0976c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0976c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0976c-141">CommonParameters</span></span>
<span data-ttu-id="0976c-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0976c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0976c-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0976c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0976c-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="0976c-144">INPUTS</span></span>

### <span data-ttu-id="0976c-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="0976c-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span></span>

### <span data-ttu-id="0976c-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="0976c-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="0976c-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0976c-147">OUTPUTS</span></span>

### <span data-ttu-id="0976c-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="0976c-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="0976c-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="0976c-149">NOTES</span></span>

<span data-ttu-id="0976c-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0976c-150">ALIASES</span></span>

<span data-ttu-id="0976c-151">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="0976c-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0976c-152">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0976c-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0976c-153">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0976c-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0976c-154">INPUTOBJECT <ICommunicationIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="0976c-154">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0976c-155">`[CommunicationServiceName <String>]`: nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="0976c-155">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="0976c-156">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="0976c-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0976c-157">`[Location <String>]`: l'area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="0976c-157">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="0976c-158">`[OperationId <String>]`: ID di un'operazione di sincronizzazione in corso</span><span class="sxs-lookup"><span data-stu-id="0976c-158">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="0976c-159">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0976c-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="0976c-160">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="0976c-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="0976c-161">`[SubscriptionId <String>]`: recupera l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0976c-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="0976c-162">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="0976c-162">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="0976c-163">PARAMETER: <IRegenerateKeyParameters> Parameters descrive la richiesta di rigenerare le chiavi di accesso</span><span class="sxs-lookup"><span data-stu-id="0976c-163">PARAMETER <IRegenerateKeyParameters>: Parameters describes the request to regenerate access keys</span></span>
  - <span data-ttu-id="0976c-164">`[KeyType <KeyType?>]`: il tipo di chiave da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="0976c-164">`[KeyType <KeyType?>]`: The keyType to regenerate.</span></span> <span data-ttu-id="0976c-165">Deve essere "principale" o "secondario" (senza distinzione tra maiuscole e minuscole).</span><span class="sxs-lookup"><span data-stu-id="0976c-165">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

## <span data-ttu-id="0976c-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0976c-166">RELATED LINKS</span></span>

