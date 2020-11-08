---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProvider.md
ms.openlocfilehash: 42b4059b146a752980b1067272713bf0a22c2c46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94193025"
---
# <span data-ttu-id="59ae8-101">Get-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="59ae8-101">Get-AzCustomProvider</span></span>

## <span data-ttu-id="59ae8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="59ae8-103">Ottiene il manifesto del provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="59ae8-103">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="59ae8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59ae8-104">SYNTAX</span></span>

### <span data-ttu-id="59ae8-105">List1 (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59ae8-105">List1 (Default)</span></span>
```
Get-AzCustomProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="59ae8-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="59ae8-106">Get</span></span>
```
Get-AzCustomProvider -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="59ae8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="59ae8-107">GetViaIdentity</span></span>
```
Get-AzCustomProvider -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="59ae8-108">Elenco</span><span class="sxs-lookup"><span data-stu-id="59ae8-108">List</span></span>
```
Get-AzCustomProvider -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="59ae8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59ae8-109">DESCRIPTION</span></span>
<span data-ttu-id="59ae8-110">Ottiene il manifesto del provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="59ae8-110">Gets the custom resource provider manifest.</span></span>

## <span data-ttu-id="59ae8-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59ae8-111">EXAMPLES</span></span>

### <span data-ttu-id="59ae8-112">Esempio 1: elencare tutti i provider personalizzati in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="59ae8-112">Example 1: List all Custom Providers in a subscription</span></span>
```powershell
PS C:\> Get-AzCustomProvider

Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
East US 2 Namespace2.Type  Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="59ae8-113">Elenca tutti i provider personalizzati in una sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="59ae8-113">Lists all the custom providers in a subscription</span></span>

### <span data-ttu-id="59ae8-114">Esempio 2: ottenere un singolo provider personalizzato</span><span class="sxs-lookup"><span data-stu-id="59ae8-114">Example 2: Get a single custom provider</span></span>
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

<span data-ttu-id="59ae8-115">Ottiene i dettagli per un singolo provider personalizzato.</span><span class="sxs-lookup"><span data-stu-id="59ae8-115">Gets details for a single custom provider.</span></span>
<span data-ttu-id="59ae8-116">Usare Format-List per visualizzare i dettagli degli oggetti sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="59ae8-116">Use Format-List to show object details on the screen.</span></span>

## <span data-ttu-id="59ae8-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59ae8-117">PARAMETERS</span></span>

### <span data-ttu-id="59ae8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59ae8-118">-DefaultProfile</span></span>
<span data-ttu-id="59ae8-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59ae8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59ae8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59ae8-120">-InputObject</span></span>
<span data-ttu-id="59ae8-121">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="59ae8-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="59ae8-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="59ae8-122">-Name</span></span>
<span data-ttu-id="59ae8-123">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="59ae8-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="59ae8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59ae8-124">-ResourceGroupName</span></span>
<span data-ttu-id="59ae8-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="59ae8-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="59ae8-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59ae8-126">-SubscriptionId</span></span>
<span data-ttu-id="59ae8-127">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="59ae8-127">The Azure subscription ID.</span></span>
<span data-ttu-id="59ae8-128">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="59ae8-128">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="59ae8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59ae8-129">CommonParameters</span></span>
<span data-ttu-id="59ae8-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59ae8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59ae8-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59ae8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59ae8-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59ae8-132">INPUTS</span></span>

### <span data-ttu-id="59ae8-133">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="59ae8-133">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="59ae8-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59ae8-134">OUTPUTS</span></span>

### <span data-ttu-id="59ae8-135">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="59ae8-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="59ae8-136">Note</span><span class="sxs-lookup"><span data-stu-id="59ae8-136">NOTES</span></span>

<span data-ttu-id="59ae8-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="59ae8-137">ALIASES</span></span>

<span data-ttu-id="59ae8-138">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59ae8-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="59ae8-139">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="59ae8-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="59ae8-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="59ae8-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="59ae8-141">INPUTOBJECT <ICustomProvidersIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="59ae8-141">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="59ae8-142">`[AssociationName <String>]`: Nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="59ae8-142">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="59ae8-143">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="59ae8-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="59ae8-144">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="59ae8-144">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="59ae8-145">`[ResourceProviderName <String>]`: Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="59ae8-145">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="59ae8-146">`[Scope <String>]`: L'ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="59ae8-146">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="59ae8-147">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="59ae8-147">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="59ae8-148">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="59ae8-148">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="59ae8-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59ae8-149">RELATED LINKS</span></span>
