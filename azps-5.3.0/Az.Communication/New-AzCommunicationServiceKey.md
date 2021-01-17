---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
ms.openlocfilehash: b97b0d640b00e2aa3b75d829464f8ebe7dd4f6d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477908"
---
# <span data-ttu-id="0537f-101">New-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="0537f-101">New-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="0537f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0537f-102">SYNOPSIS</span></span>
<span data-ttu-id="0537f-103">Tasto di accesso rigenera CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="0537f-103">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="0537f-104">PrimaryKey e SecondaryKey non possono essere rigenerati simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="0537f-104">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="0537f-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0537f-105">SYNTAX</span></span>

### <span data-ttu-id="0537f-106">RegenerateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0537f-106">RegenerateExpanded (Default)</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyType <KeyType>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0537f-107">Rigenerare</span><span class="sxs-lookup"><span data-stu-id="0537f-107">Regenerate</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 -Parameter <IRegenerateKeyParameters> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0537f-108">RegenerateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0537f-108">RegenerateViaIdentity</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> -Parameter <IRegenerateKeyParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0537f-109">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0537f-109">RegenerateViaIdentityExpanded</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> [-KeyType <KeyType>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0537f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0537f-110">DESCRIPTION</span></span>
<span data-ttu-id="0537f-111">Tasto di accesso rigenera CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="0537f-111">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="0537f-112">PrimaryKey e SecondaryKey non possono essere rigenerati simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="0537f-112">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="0537f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0537f-113">EXAMPLES</span></span>

### <span data-ttu-id="0537f-114">Esempio 1: rigenera la chiave primaria usando una Hashtable IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="0537f-114">Example 1: Regenerates the Primary key using a IRegenerateKeyParameters hashtable</span></span>
```powershell
PS > New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Parameter @{KeyType="Primary"}

PrimaryConnectionString              PrimaryKey
-----------------------              ----------
endpoint=<example-primary-endpoint>  <example-primarykey>
```

<span data-ttu-id="0537f-115">Invalida la chiave primaria precedente, rigenerarne una nuova e restituirla.</span><span class="sxs-lookup"><span data-stu-id="0537f-115">Invalidates the previous Primary key, regenerate a new one and return it.</span></span>

### <span data-ttu-id="0537f-116">Esempio 2: rigenera la chiave secondaria usando un tipo di tasti</span><span class="sxs-lookup"><span data-stu-id="0537f-116">Example 2: Regenerates the Secondary key using a KeyType</span></span>
```powershell
PS C:\> New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -KeyType Secondary

SecondaryConnectionString               SecondaryKey
-----------------------                 ----------
endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="0537f-117">Invalida la chiave secondaria precedente, rigenerarne una nuova e restituirla.</span><span class="sxs-lookup"><span data-stu-id="0537f-117">Invalidates the previous Secondary key, regenerate a new one and return it.</span></span>

## <span data-ttu-id="0537f-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0537f-118">PARAMETERS</span></span>

### <span data-ttu-id="0537f-119">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="0537f-119">-CommunicationServiceName</span></span>
<span data-ttu-id="0537f-120">Il nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="0537f-120">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="0537f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0537f-121">-DefaultProfile</span></span>
<span data-ttu-id="0537f-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0537f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0537f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0537f-123">-InputObject</span></span>
<span data-ttu-id="0537f-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0537f-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0537f-125">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="0537f-125">-KeyType</span></span>
<span data-ttu-id="0537f-126">Il tipo di digitare da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="0537f-126">The keyType to regenerate.</span></span>
<span data-ttu-id="0537f-127">Deve essere "Primary" o "Secondary" (senza distinzione tra maiuscole e minuscole).</span><span class="sxs-lookup"><span data-stu-id="0537f-127">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

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

### <span data-ttu-id="0537f-128">Parametro-</span><span class="sxs-lookup"><span data-stu-id="0537f-128">-Parameter</span></span>
<span data-ttu-id="0537f-129">Parameters descrive la richiesta di rigenerare i tasti di scelta per la creazione, vedere la sezione Note per le proprietà dei parametri e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0537f-129">Parameters describes the request to regenerate access keys To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="0537f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0537f-130">-ResourceGroupName</span></span>
<span data-ttu-id="0537f-131">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0537f-131">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0537f-132">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="0537f-132">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0537f-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0537f-133">-SubscriptionId</span></span>
<span data-ttu-id="0537f-134">Ottiene l'ID abbonamento che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0537f-134">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0537f-135">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="0537f-135">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0537f-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0537f-136">-Confirm</span></span>
<span data-ttu-id="0537f-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0537f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0537f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0537f-138">-WhatIf</span></span>
<span data-ttu-id="0537f-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0537f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0537f-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0537f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0537f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0537f-141">CommonParameters</span></span>
<span data-ttu-id="0537f-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0537f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0537f-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0537f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0537f-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0537f-144">INPUTS</span></span>

### <span data-ttu-id="0537f-145">Microsoft. Azure. PowerShell. Cmdlets. Communication. Models. Api20200820Preview. IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="0537f-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span></span>

### <span data-ttu-id="0537f-146">Microsoft. Azure. PowerShell. Cmdlets. Communication. Models. ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="0537f-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="0537f-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0537f-147">OUTPUTS</span></span>

### <span data-ttu-id="0537f-148">Microsoft. Azure. PowerShell. Cmdlets. Communication. Models. Api20200820Preview. ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="0537f-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="0537f-149">Note</span><span class="sxs-lookup"><span data-stu-id="0537f-149">NOTES</span></span>

<span data-ttu-id="0537f-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0537f-150">ALIASES</span></span>

<span data-ttu-id="0537f-151">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0537f-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0537f-152">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0537f-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0537f-153">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0537f-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0537f-154">INPUTOBJECT <ICommunicationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="0537f-154">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0537f-155">`[CommunicationServiceName <String>]`: Il nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="0537f-155">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="0537f-156">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="0537f-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0537f-157">`[Location <String>]`: Area di Azure</span><span class="sxs-lookup"><span data-stu-id="0537f-157">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="0537f-158">`[OperationId <String>]`: ID di un'operazione asincrona in corso</span><span class="sxs-lookup"><span data-stu-id="0537f-158">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="0537f-159">`[ResourceGroupName <String>]`: Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0537f-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="0537f-160">Puoi ottenere questo valore dall'API di gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="0537f-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="0537f-161">`[SubscriptionId <String>]`: Ottiene l'ID sottoscrizione che identifica in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0537f-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="0537f-162">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="0537f-162">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="0537f-163">PARAMETER <IRegenerateKeyParameters> : Parameters descrive la richiesta di rigenerare i tasti di scelta</span><span class="sxs-lookup"><span data-stu-id="0537f-163">PARAMETER <IRegenerateKeyParameters>: Parameters describes the request to regenerate access keys</span></span>
  - <span data-ttu-id="0537f-164">`[KeyType <KeyType?>]`: Il tipo di digitare da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="0537f-164">`[KeyType <KeyType?>]`: The keyType to regenerate.</span></span> <span data-ttu-id="0537f-165">Deve essere "Primary" o "Secondary" (senza distinzione tra maiuscole e minuscole).</span><span class="sxs-lookup"><span data-stu-id="0537f-165">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

## <span data-ttu-id="0537f-166">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0537f-166">RELATED LINKS</span></span>

