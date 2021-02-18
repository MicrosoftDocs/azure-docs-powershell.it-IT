---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 42b4059b146a752980b1067272713bf0a22c2c46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181159"
---
# <span data-ttu-id="6e3be-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="6e3be-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="6e3be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e3be-102">SYNOPSIS</span></span>
<span data-ttu-id="6e3be-103">Ottiene il manifesto del provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="6e3be-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="6e3be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e3be-104">SYNTAX</span></span>

### <span data-ttu-id="6e3be-105">Elenco1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6e3be-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6e3be-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="6e3be-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6e3be-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6e3be-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6e3be-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="6e3be-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e3be-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6e3be-109">DESCRIPTION</span></span>
<span data-ttu-id="6e3be-110">Ottiene il manifesto del provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="6e3be-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="6e3be-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e3be-111">EXAMPLES</span></span>

### <span data-ttu-id="6e3be-112">Esempio 1: Elencare tutti i provider personalizzati in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="6e3be-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="6e3be-113">Elenca tutti i provider personalizzati di una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="6e3be-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="6e3be-114">Esempio 2: Ottenere un singolo provider personalizzato</span><span class="sxs-lookup"><span data-stu-id="6e3be-114">Example 2: Get a single custom provider</span></span>
```powershell
PS C:\> Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type | Format-List

Action            :
Id                : /subscriptions/xxxxx-yyyyy-xxxx-yyyy/resourceGroups/mc-cp01/providers/Microsoft.CustomProviders/resourceproviders/Namespace.Type
Location          : West US 2
Name              : Namespace.Type
ProvisioningState : Succeeded
ResourceType      : {CustomRoute1, associations}
Tag               : Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ResourceTags
Type              : Microsoft.CustomProviders/resourceproviders
Validation        :

```

<span data-ttu-id="6e3be-115">Recupera i dettagli per un singolo provider personalizzato.</span><span class="sxs-lookup"><span data-stu-id="6e3be-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="6e3be-116">Usare Format-List per visualizzare i dettagli degli oggetti sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="6e3be-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="6e3be-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e3be-117">PARAMETERS</span></span>

### <span data-ttu-id="6e3be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e3be-118">-DefaultProfile</span></span>
<span data-ttu-id="6e3be-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e3be-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e3be-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e3be-120">-InputObject</span></span>
<span data-ttu-id="6e3be-121">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6e3be-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e3be-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6e3be-122">-Name</span></span>
<span data-ttu-id="6e3be-123">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="6e3be-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e3be-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e3be-124">-ResourceGroupName</span></span>
<span data-ttu-id="6e3be-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6e3be-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e3be-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e3be-126">-SubscriptionId</span></span>
<span data-ttu-id="6e3be-127">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6e3be-127">The Azure subscription ID.</span></span>
<span data-ttu-id="6e3be-128">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-00000000000000</span><span class="sxs-lookup"><span data-stu-id="6e3be-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="6e3be-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e3be-129">CommonParameters</span></span>
<span data-ttu-id="6e3be-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e3be-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e3be-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6e3be-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e3be-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="6e3be-132">INPUTS</span></span>

### <span data-ttu-id="6e3be-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="6e3be-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="6e3be-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e3be-134">OUTPUTS</span></span>

### <span data-ttu-id="6e3be-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="6e3be-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="6e3be-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="6e3be-136">NOTES</span></span>

<span data-ttu-id="6e3be-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6e3be-137">ALIASES</span></span>

<span data-ttu-id="6e3be-138">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="6e3be-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6e3be-139">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="6e3be-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6e3be-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6e3be-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6e3be-141">INPUTOBJECT <ICustomProvidersIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="6e3be-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6e3be-142">`[AssociationName <String>]`: nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="6e3be-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="6e3be-143">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="6e3be-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6e3be-144">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6e3be-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6e3be-145">`[ResourceProviderName <String>]`: nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="6e3be-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="6e3be-146">`[Scope <String>]`: ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="6e3be-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="6e3be-147">`[SubscriptionId <String>]`: l'ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6e3be-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="6e3be-148">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-00000000000000</span><span class="sxs-lookup"><span data-stu-id="6e3be-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="6e3be-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e3be-149">RELATED LINKS</span></span>

