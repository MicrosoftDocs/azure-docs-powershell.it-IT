---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/get-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
ms.openlocfilehash: f9f4cc86a07c50718511c3ed0889d96f7acec9a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991673"
---
# <span data-ttu-id="614ec-101">Get-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="614ec-101">Get-AzCommunicationService</span></span>

## <span data-ttu-id="614ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="614ec-102">SYNOPSIS</span></span>
<span data-ttu-id="614ec-103">Ottenere CommunicationService e le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="614ec-103">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="614ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="614ec-104">SYNTAX</span></span>

### <span data-ttu-id="614ec-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="614ec-105">List (Default)</span></span>
```
Get-AzCommunicationService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="614ec-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="614ec-106">Get</span></span>
```
Get-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="614ec-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="614ec-107">GetViaIdentity</span></span>
```
Get-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="614ec-108">Elenco1</span><span class="sxs-lookup"><span data-stu-id="614ec-108">List1</span></span>
```
Get-AzCommunicationService -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="614ec-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="614ec-109">DESCRIPTION</span></span>
<span data-ttu-id="614ec-110">Ottenere CommunicationService e le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="614ec-110">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="614ec-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="614ec-111">EXAMPLES</span></span>

### <span data-ttu-id="614ec-112">Esempio 1: Elencare i servizi di comunicazione esistenti per una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="614ec-112">Example 1: List existing CommunicationServices for a Subscription</span></span>
```powershell
PS C:\> Get-AzCommunicationService -SubscriptionId 73fc3592-3cef-4300-5e19-8d18b65ce0e8

Location Name             Type                                          AzureAsyncOperation
-------- ----             ----                                          -------------------
global   ContosoResource1   Microsoft.Communication/communicationServices
global   ContosoResource4   Microsoft.Communication/communicationServices
global   ContosoResource3   Microsoft.Communication/communicationServices
global   ContosoResource5   Microsoft.Communication/communicationServices
```

<span data-ttu-id="614ec-113">Restituisce un elenco di tutte le risorse ACS nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="614ec-113">Returns a list of all ACS resources under that subscription.</span></span>

### <span data-ttu-id="614ec-114">Esempio 2: Ottenere informazioni sulla risorsa di comunicazione di Azure specificata</span><span class="sxs-lookup"><span data-stu-id="614ec-114">Example 2: Get infomation on specified Azure Communication resource</span></span>
```powershell
PS C:\> Get-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="614ec-115">Restituisce le informazioni su una risorsa ACS, se viene trovato un parametro fornito corrispondente.</span><span class="sxs-lookup"><span data-stu-id="614ec-115">Returns the information on an ACS resource, if one matching provided parameters is found.</span></span>

## <span data-ttu-id="614ec-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="614ec-116">PARAMETERS</span></span>

### <span data-ttu-id="614ec-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="614ec-117">-DefaultProfile</span></span>
<span data-ttu-id="614ec-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="614ec-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="614ec-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="614ec-119">-InputObject</span></span>
<span data-ttu-id="614ec-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="614ec-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="614ec-121">-Name</span><span class="sxs-lookup"><span data-stu-id="614ec-121">-Name</span></span>
<span data-ttu-id="614ec-122">Nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="614ec-122">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="614ec-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="614ec-123">-ResourceGroupName</span></span>
<span data-ttu-id="614ec-124">Nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="614ec-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="614ec-125">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="614ec-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="614ec-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="614ec-126">-SubscriptionId</span></span>
<span data-ttu-id="614ec-127">Ottiene l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="614ec-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="614ec-128">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="614ec-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="614ec-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="614ec-129">CommonParameters</span></span>
<span data-ttu-id="614ec-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="614ec-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="614ec-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="614ec-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="614ec-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="614ec-132">INPUTS</span></span>

### <span data-ttu-id="614ec-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="614ec-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="614ec-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="614ec-134">OUTPUTS</span></span>

### <span data-ttu-id="614ec-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="614ec-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="614ec-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="614ec-136">NOTES</span></span>

<span data-ttu-id="614ec-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="614ec-137">ALIASES</span></span>

<span data-ttu-id="614ec-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="614ec-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="614ec-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="614ec-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="614ec-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="614ec-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="614ec-141">INPUTOBJECT <ICommunicationIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="614ec-141">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="614ec-142">`[CommunicationServiceName <String>]`: nome della risorsa CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="614ec-142">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="614ec-143">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="614ec-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="614ec-144">`[Location <String>]`: l'area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="614ec-144">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="614ec-145">`[OperationId <String>]`: ID di un'operazione di sincronizzazione in corso</span><span class="sxs-lookup"><span data-stu-id="614ec-145">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="614ec-146">`[ResourceGroupName <String>]`: nome del gruppo di risorse che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="614ec-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="614ec-147">È possibile ottenere questo valore dall'API di Gestione risorse di Azure o dal portale.</span><span class="sxs-lookup"><span data-stu-id="614ec-147">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="614ec-148">`[SubscriptionId <String>]`: recupera l'ID sottoscrizione che identifica in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="614ec-148">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="614ec-149">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="614ec-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="614ec-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="614ec-150">RELATED LINKS</span></span>

