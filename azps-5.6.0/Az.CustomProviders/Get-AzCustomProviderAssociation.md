---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: f7c36ca53b00c0fc99e5afc6e6ba74f4cff62afb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998785"
---
# <span data-ttu-id="020af-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="020af-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="020af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="020af-102">SYNOPSIS</span></span>
<span data-ttu-id="020af-103">Ottenere un'associazione.</span><span class="sxs-lookup"><span data-stu-id="020af-103">Get an association.</span></span>

## <span data-ttu-id="020af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="020af-104">SYNTAX</span></span>

### <span data-ttu-id="020af-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="020af-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="020af-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="020af-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="020af-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="020af-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="020af-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="020af-108">DESCRIPTION</span></span>
<span data-ttu-id="020af-109">Ottenere un'associazione.</span><span class="sxs-lookup"><span data-stu-id="020af-109">Get an association.</span></span>

## <span data-ttu-id="020af-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="020af-110">EXAMPLES</span></span>

### <span data-ttu-id="020af-111">Esempio 1: Elencare le associazioni di provider personalizzate</span><span class="sxs-lookup"><span data-stu-id="020af-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="020af-112">Elencare tutte le associazioni di provider personalizzate per un determinato ambito.</span><span class="sxs-lookup"><span data-stu-id="020af-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="020af-113">Esempio 2: Ottenere un'associazione</span><span class="sxs-lookup"><span data-stu-id="020af-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="020af-114">Ottenere i dettagli per una singola associazione CustomProvider</span><span class="sxs-lookup"><span data-stu-id="020af-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="020af-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="020af-115">PARAMETERS</span></span>

### <span data-ttu-id="020af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="020af-116">-DefaultProfile</span></span>
<span data-ttu-id="020af-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="020af-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="020af-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="020af-118">-InputObject</span></span>
<span data-ttu-id="020af-119">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="020af-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="020af-120">-Name</span><span class="sxs-lookup"><span data-stu-id="020af-120">-Name</span></span>
<span data-ttu-id="020af-121">Nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="020af-121">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="020af-122">-Scope</span><span class="sxs-lookup"><span data-stu-id="020af-122">-Scope</span></span>
<span data-ttu-id="020af-123">Ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="020af-123">The scope of the association.</span></span>

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

### <span data-ttu-id="020af-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="020af-124">CommonParameters</span></span>
<span data-ttu-id="020af-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="020af-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="020af-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="020af-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="020af-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="020af-127">INPUTS</span></span>

### <span data-ttu-id="020af-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="020af-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="020af-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="020af-129">OUTPUTS</span></span>

### <span data-ttu-id="020af-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="020af-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="020af-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="020af-131">NOTES</span></span>

<span data-ttu-id="020af-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="020af-132">ALIASES</span></span>

<span data-ttu-id="020af-133">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="020af-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="020af-134">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="020af-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="020af-135">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="020af-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="020af-136">INPUTOBJECT <ICustomProvidersIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="020af-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="020af-137">`[AssociationName <String>]`: nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="020af-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="020af-138">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="020af-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="020af-139">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="020af-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="020af-140">`[ResourceProviderName <String>]`: nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="020af-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="020af-141">`[Scope <String>]`: ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="020af-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="020af-142">`[SubscriptionId <String>]`: ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="020af-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="020af-143">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-00000000000000</span><span class="sxs-lookup"><span data-stu-id="020af-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="020af-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="020af-144">RELATED LINKS</span></span>

