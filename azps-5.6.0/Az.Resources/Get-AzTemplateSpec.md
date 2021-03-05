---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: 0b2018eecc081f2fcee5da63ed17cc2e01486777
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960110"
---
# <span data-ttu-id="b5c1a-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="b5c1a-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="b5c1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5c1a-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c1a-103">Ottiene o elenca le specifiche del modello</span><span class="sxs-lookup"><span data-stu-id="b5c1a-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="b5c1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5c1a-104">SYNTAX</span></span>

### <span data-ttu-id="b5c1a-105">ListTemplateSpecsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5c1a-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5c1a-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5c1a-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5c1a-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5c1a-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5c1a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b5c1a-108">DESCRIPTION</span></span>
<span data-ttu-id="b5c1a-109">Questo cmdlet può essere usato per elencare le specifiche dei modelli in un gruppo di sottoscrizioni/risorse o ottenere specifiche del modello in base al nome o all'ID. Se si riceve una specifica per nome/ID, è possibile recuperare una versione specifica specificando un nome di versione tramite il **parametro -Version.**</span><span class="sxs-lookup"><span data-stu-id="b5c1a-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="b5c1a-110">Quando **si usa -Version,** saranno presenti solo i dettagli della versione specifici all'interno di \**. Versioni nell'oggetto* spec del modello restituito.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-110">When **-Version** is used, only the specific version details will be present within \**.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="b5c1a-111">Se non viene specificata alcuna versione specifica durante il recupero di una specifica modello per nome/id, tutte le versioni saranno presenti all'interno di \**. Proprietà Versions* dell'oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \**.Versions* property of the returned object.</span></span>

<span data-ttu-id="b5c1a-112">**Nota:** quando si elencano tutte le specifiche del modello all'interno di una sottoscrizione o di un gruppo di risorse, vengono restituite specifiche del *modello " . Versions"* sarà *Null.*</span><span class="sxs-lookup"><span data-stu-id="b5c1a-112">**Note**: When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="b5c1a-113">Le informazioni sulla versione vengono incluse solo quando vengono forniti parametri -Name o -ResourceId (ad esempio, si richiede una specifica o versione del modello).</span><span class="sxs-lookup"><span data-stu-id="b5c1a-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="b5c1a-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5c1a-114">EXAMPLES</span></span>

### <span data-ttu-id="b5c1a-115">Esempio 1: Specifiche del modello di elenco nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="b5c1a-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="b5c1a-116">Elenca tutte le specifiche dei modelli nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="b5c1a-117">Esempio 2: Specifiche del modello di elenco in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b5c1a-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="b5c1a-118">Elenca tutte le specifiche dei modelli nel gruppo di risorse "myRG" della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="b5c1a-119">Esempio 3: Ottenere le specifiche del modello (con tutte le versioni) in base al nome</span><span class="sxs-lookup"><span data-stu-id="b5c1a-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="b5c1a-120">Ottiene informazioni sulla specifica del modello denominata "MyTemplateSpec" all'interno del gruppo di risorse "myRG".</span><span class="sxs-lookup"><span data-stu-id="b5c1a-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="b5c1a-121">**Nota:** tutte le versioni delle specifiche del modello saranno presenti all'interno di "*. Versions*" proprietà dell'oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-121">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="b5c1a-122">Esempio 4: Ottenere le specifiche del modello (versione specifica) in base al nome</span><span class="sxs-lookup"><span data-stu-id="b5c1a-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="b5c1a-123">Ottiene informazioni sulla versione "v1.0" della specifica di modello denominata "MyTemplateSpec" all'interno del gruppo di risorse "myRG".</span><span class="sxs-lookup"><span data-stu-id="b5c1a-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="b5c1a-124">**Nota:** *". Versions"* dell'oggetto restituito conterrà solo la versione specifica richiesta.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-124">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="b5c1a-125">Esempio 5: Ottenere le specifiche del modello (con tutte le versioni) in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="b5c1a-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="b5c1a-126">Ottiene informazioni sulla specifica del modello denominata "MyTemplateSpec" all'interno del gruppo di risorse "myRG" del \{ subId della \} sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="b5c1a-127">**Nota:** tutte le versioni delle specifiche del modello saranno presenti all'interno di "*. Versions*" proprietà dell'oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-127">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="b5c1a-128">Esempio 6: Ottenere le specifiche del modello (versione specifica) in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="b5c1a-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="b5c1a-129">Ottiene informazioni sulla versione 'v1.0' della specifica di modello denominata "MyTemplateSpec" all'interno del gruppo di risorse 'myRG' di \{ subscription \} subId.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="b5c1a-130">**Nota:** *". Versions"* dell'oggetto restituito conterrà solo la versione specifica richiesta.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-130">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="b5c1a-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5c1a-131">PARAMETERS</span></span>

### <span data-ttu-id="b5c1a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c1a-132">-DefaultProfile</span></span>
<span data-ttu-id="b5c1a-133">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5c1a-134">-Name</span><span class="sxs-lookup"><span data-stu-id="b5c1a-134">-Name</span></span>
<span data-ttu-id="b5c1a-135">Nome della specifica di modello.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-135">The name of the template spec.</span></span>

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

### <span data-ttu-id="b5c1a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5c1a-136">-ResourceGroupName</span></span>
<span data-ttu-id="b5c1a-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="b5c1a-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5c1a-138">-ResourceId</span></span>
<span data-ttu-id="b5c1a-139">ID risorsa completo della specifica del modello. Esempio: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="b5c1a-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="b5c1a-140">-Version</span><span class="sxs-lookup"><span data-stu-id="b5c1a-140">-Version</span></span>
<span data-ttu-id="b5c1a-141">Versione delle specifiche del modello.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-141">The version of the template spec.</span></span>

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

### <span data-ttu-id="b5c1a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c1a-142">CommonParameters</span></span>
<span data-ttu-id="b5c1a-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c1a-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b5c1a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c1a-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="b5c1a-145">INPUTS</span></span>

### <span data-ttu-id="b5c1a-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b5c1a-146">System.String</span></span>

## <span data-ttu-id="b5c1a-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5c1a-147">OUTPUTS</span></span>

### <span data-ttu-id="b5c1a-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="b5c1a-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="b5c1a-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="b5c1a-149">NOTES</span></span>

## <span data-ttu-id="b5c1a-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5c1a-150">RELATED LINKS</span></span>
