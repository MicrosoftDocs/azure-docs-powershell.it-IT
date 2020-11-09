---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301074"
---
# <span data-ttu-id="95d6f-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="95d6f-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="95d6f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="95d6f-103">Ottiene o elenca le specifiche del modello</span><span class="sxs-lookup"><span data-stu-id="95d6f-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="95d6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95d6f-104">SYNTAX</span></span>

### <span data-ttu-id="95d6f-105">ListTemplateSpecsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="95d6f-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95d6f-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="95d6f-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95d6f-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95d6f-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95d6f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95d6f-108">DESCRIPTION</span></span>
<span data-ttu-id="95d6f-109">Questo cmdlet può essere usato per elencare le specifiche di un modello in un gruppo di abbonamenti/risorse o per ottenere una specifica specifiche del modello per nome o ID. Quando si riceve un modello specifico per nome/ID, è possibile recuperare facoltativamente una versione specifica specificando un nome di versione tramite il parametro **-Version** .</span><span class="sxs-lookup"><span data-stu-id="95d6f-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="95d6f-110">Quando viene usata la **versione** , solo i dettagli specifici della versione saranno presenti in \* *. Versioni* nell'oggetto spec modello restituito.</span><span class="sxs-lookup"><span data-stu-id="95d6f-110">When **-Version** is used, only the specific version details will be present within \* *.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="95d6f-111">Se non viene specificata una versione specifica durante il recupero di una specifica modello per nome/ID, tutte le versioni saranno presenti all'interno di \* *. Proprietà Versions* dell'oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="95d6f-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \* *.Versions* property of the returned object.</span></span>

<span data-ttu-id="95d6f-112">**Nota** : quando si elencano tutte le specifiche del modello all'interno di un gruppo di abbonamenti o risorse, ogni specifica di modello restituita è *". La proprietà Versions* sarà *null*.</span><span class="sxs-lookup"><span data-stu-id="95d6f-112">**Note** : When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="95d6f-113">Le informazioni sulla versione sono incluse solo quando-Name oppure-i parametri ResourceId sono disponibili (ad esempio: si richiede una specifica/versione del modello specifico).</span><span class="sxs-lookup"><span data-stu-id="95d6f-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="95d6f-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95d6f-114">EXAMPLES</span></span>

### <span data-ttu-id="95d6f-115">Esempio 1: specifiche del modello di elenco nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="95d6f-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="95d6f-116">Elenca tutte le specifiche del modello nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="95d6f-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="95d6f-117">Esempio 2: specifiche del modello di elenco in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="95d6f-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="95d6f-118">Elenca tutte le specifiche del modello nel gruppo di risorse "myRG" della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="95d6f-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="95d6f-119">Esempio 3: ottenere la specifica del modello (con tutte le versioni) per nome</span><span class="sxs-lookup"><span data-stu-id="95d6f-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="95d6f-120">Ottiene informazioni sulla specifica del modello denominata "MyTemplateSpec" nel gruppo di risorse "myRG".</span><span class="sxs-lookup"><span data-stu-id="95d6f-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="95d6f-121">**Nota** : tutte le versioni della specifica del modello saranno presenti all'interno del " *. Proprietà Versions* dell'oggetto return.</span><span class="sxs-lookup"><span data-stu-id="95d6f-121">**Note** : All of the Template Spec's versions will be present within the " *.Versions* " property of the return object.</span></span>

### <span data-ttu-id="95d6f-122">Esempio 4: ottenere la specifica del modello (versione specifica) per nome</span><span class="sxs-lookup"><span data-stu-id="95d6f-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="95d6f-123">Ottiene le informazioni sulla versione "v 1.0" della specifica del modello denominata "MyTemplateSpec" nel gruppo di risorse "myRG".</span><span class="sxs-lookup"><span data-stu-id="95d6f-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="95d6f-124">**Nota** : *". La proprietà Versions* dell'oggetto restituito conterrà solo la versione specifica richiesta.</span><span class="sxs-lookup"><span data-stu-id="95d6f-124">**Note** : The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="95d6f-125">Esempio 5: ottenere la specifica del modello (con tutte le versioni) per ID risorsa</span><span class="sxs-lookup"><span data-stu-id="95d6f-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="95d6f-126">Ottiene le informazioni sulla specifica del modello denominata "MyTemplateSpec" nel gruppo di risorse "myRG" dell'abbonamento \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="95d6f-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="95d6f-127">**Nota** : tutte le versioni della specifica del modello saranno presenti all'interno del " *. Proprietà Versions* dell'oggetto return.</span><span class="sxs-lookup"><span data-stu-id="95d6f-127">**Note** : All of the Template Spec's versions will be present within the " *.Versions* " property of the return object.</span></span>

### <span data-ttu-id="95d6f-128">Esempio 6: ottenere la specifica del modello (versione specifica) per ID risorsa</span><span class="sxs-lookup"><span data-stu-id="95d6f-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="95d6f-129">Ottiene le informazioni sulla versione "v 1.0" della specifica del modello denominata "MyTemplateSpec" nel gruppo di risorse "myRG" della sottoscrizione di \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="95d6f-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="95d6f-130">**Nota** : *". La proprietà Versions* dell'oggetto restituito conterrà solo la versione specifica richiesta.</span><span class="sxs-lookup"><span data-stu-id="95d6f-130">**Note** : The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="95d6f-131">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95d6f-131">PARAMETERS</span></span>

### <span data-ttu-id="95d6f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d6f-132">-DefaultProfile</span></span>
<span data-ttu-id="95d6f-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95d6f-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95d6f-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="95d6f-134">-Name</span></span>
<span data-ttu-id="95d6f-135">Nome della specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="95d6f-135">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d6f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95d6f-136">-ResourceGroupName</span></span>
<span data-ttu-id="95d6f-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="95d6f-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d6f-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95d6f-138">-ResourceId</span></span>
<span data-ttu-id="95d6f-139">ID risorsa completo del modello spec. esempio:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="95d6f-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d6f-140">-Versione</span><span class="sxs-lookup"><span data-stu-id="95d6f-140">-Version</span></span>
<span data-ttu-id="95d6f-141">Versione della specifica del modello.</span><span class="sxs-lookup"><span data-stu-id="95d6f-141">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d6f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d6f-142">CommonParameters</span></span>
<span data-ttu-id="95d6f-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95d6f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d6f-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95d6f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d6f-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95d6f-145">INPUTS</span></span>

### <span data-ttu-id="95d6f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="95d6f-146">System.String</span></span>

## <span data-ttu-id="95d6f-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95d6f-147">OUTPUTS</span></span>

### <span data-ttu-id="95d6f-148">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="95d6f-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="95d6f-149">Note</span><span class="sxs-lookup"><span data-stu-id="95d6f-149">NOTES</span></span>

## <span data-ttu-id="95d6f-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95d6f-150">RELATED LINKS</span></span>
