---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/get-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/Get-AzCustomProviderAssociation.md
ms.openlocfilehash: 08d760c73256b71842fac36a7d095db2aab21128
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369176"
---
# <span data-ttu-id="47b5f-101">Get-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="47b5f-101">Get-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="47b5f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47b5f-102">SYNOPSIS</span></span>
<span data-ttu-id="47b5f-103">Ottenere un'associazione.</span><span class="sxs-lookup"><span data-stu-id="47b5f-103">Get an association.</span></span>

## <span data-ttu-id="47b5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47b5f-104">SYNTAX</span></span>

### <span data-ttu-id="47b5f-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="47b5f-105">List (Default)</span></span>
```
Get-AzCustomProviderAssociation -Scope <String> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="47b5f-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="47b5f-106">Get</span></span>
```
Get-AzCustomProviderAssociation -Name <String> -Scope <String> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="47b5f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="47b5f-107">GetViaIdentity</span></span>
```
Get-AzCustomProviderAssociation -InputObject <ICustomProvidersIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="47b5f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47b5f-108">DESCRIPTION</span></span>
<span data-ttu-id="47b5f-109">Ottenere un'associazione.</span><span class="sxs-lookup"><span data-stu-id="47b5f-109">Get an association.</span></span>

## <span data-ttu-id="47b5f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47b5f-110">EXAMPLES</span></span>

### <span data-ttu-id="47b5f-111">Esempio 1: elencare associazioni di provider personalizzate</span><span class="sxs-lookup"><span data-stu-id="47b5f-111">Example 1: List custom provider associations</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="47b5f-112">Elenca tutte le associazioni di provider personalizzate per un ambito specifico.</span><span class="sxs-lookup"><span data-stu-id="47b5f-112">List all custom provider associations for a given scope.</span></span>

### <span data-ttu-id="47b5f-113">Esempio 2: ottenere un'associazione</span><span class="sxs-lookup"><span data-stu-id="47b5f-113">Example 2: Get an association</span></span>
```powershell
PS C:\> Get-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc

Location  Name             Type
--------  ----             ----
East US 2 MyAssoc   Microsoft.CustomProviders/associations
```

<span data-ttu-id="47b5f-114">Ottenere informazioni dettagliate per una singola associazione CustomProvider</span><span class="sxs-lookup"><span data-stu-id="47b5f-114">Get details for a single CustomProvider association</span></span>

## <span data-ttu-id="47b5f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47b5f-115">PARAMETERS</span></span>

### <span data-ttu-id="47b5f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b5f-116">-DefaultProfile</span></span>
<span data-ttu-id="47b5f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47b5f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47b5f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47b5f-118">-InputObject</span></span>
<span data-ttu-id="47b5f-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="47b5f-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="47b5f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="47b5f-120">-Name</span></span>
<span data-ttu-id="47b5f-121">Nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="47b5f-121">The name of the association.</span></span>

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

### <span data-ttu-id="47b5f-122">-Ambito</span><span class="sxs-lookup"><span data-stu-id="47b5f-122">-Scope</span></span>
<span data-ttu-id="47b5f-123">Ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="47b5f-123">The scope of the association.</span></span>

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

### <span data-ttu-id="47b5f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b5f-124">CommonParameters</span></span>
<span data-ttu-id="47b5f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47b5f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b5f-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47b5f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b5f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47b5f-127">INPUTS</span></span>

### <span data-ttu-id="47b5f-128">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. ICustomProvidersIdentity</span><span class="sxs-lookup"><span data-stu-id="47b5f-128">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.ICustomProvidersIdentity</span></span>

## <span data-ttu-id="47b5f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47b5f-129">OUTPUTS</span></span>

### <span data-ttu-id="47b5f-130">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. Api20180901Preview. IAssociation</span><span class="sxs-lookup"><span data-stu-id="47b5f-130">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="47b5f-131">Note</span><span class="sxs-lookup"><span data-stu-id="47b5f-131">NOTES</span></span>

<span data-ttu-id="47b5f-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="47b5f-132">ALIASES</span></span>

<span data-ttu-id="47b5f-133">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47b5f-133">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="47b5f-134">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="47b5f-134">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47b5f-135">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="47b5f-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="47b5f-136">INPUTOBJECT <ICustomProvidersIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="47b5f-136">INPUTOBJECT <ICustomProvidersIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="47b5f-137">`[AssociationName <String>]`: Nome dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="47b5f-137">`[AssociationName <String>]`: The name of the association.</span></span>
  - <span data-ttu-id="47b5f-138">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="47b5f-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="47b5f-139">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="47b5f-139">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="47b5f-140">`[ResourceProviderName <String>]`: Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="47b5f-140">`[ResourceProviderName <String>]`: The name of the resource provider.</span></span>
  - <span data-ttu-id="47b5f-141">`[Scope <String>]`: L'ambito dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="47b5f-141">`[Scope <String>]`: The scope of the association.</span></span>
  - <span data-ttu-id="47b5f-142">`[SubscriptionId <String>]`: ID abbonamento Azure.</span><span class="sxs-lookup"><span data-stu-id="47b5f-142">`[SubscriptionId <String>]`: The Azure subscription ID.</span></span> <span data-ttu-id="47b5f-143">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="47b5f-143">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

## <span data-ttu-id="47b5f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47b5f-144">RELATED LINKS</span></span>

