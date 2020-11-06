---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 8914b6d48b14ea372f29a6b7b0f5c9a1c32a6fd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507991"
---
# <span data-ttu-id="eb955-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="eb955-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="eb955-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb955-102">SYNOPSIS</span></span>
<span data-ttu-id="eb955-103">Definizione dell'applicazione gestita degli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="eb955-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb955-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb955-104">SYNTAX</span></span>

### <span data-ttu-id="eb955-105">SetByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eb955-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eb955-106">SetById</span><span class="sxs-lookup"><span data-stu-id="eb955-106">SetById</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb955-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb955-107">DESCRIPTION</span></span>
<span data-ttu-id="eb955-108">Il cmdlet **set-AzureRmManagedApplicationDefinition** aggiorna le definizioni delle applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="eb955-108">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="eb955-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb955-109">EXAMPLES</span></span>

### <span data-ttu-id="eb955-110">Esempio 1: aggiornare la descrizione della definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="eb955-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="eb955-111">Questo comando Aggiorna la descrizione della definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="eb955-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="eb955-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb955-112">PARAMETERS</span></span>

### <span data-ttu-id="eb955-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="eb955-113">-ApiVersion</span></span>
<span data-ttu-id="eb955-114">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="eb955-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="eb955-115">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="eb955-115">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb955-116">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="eb955-116">-Authorization</span></span>
<span data-ttu-id="eb955-117">Autorizzazione per la definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="eb955-117">The managed application definition authorization.</span></span>
<span data-ttu-id="eb955-118">Coppie di autorizzazioni separate da virgola in un formato di \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="eb955-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb955-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb955-119">-DefaultProfile</span></span>
<span data-ttu-id="eb955-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb955-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb955-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb955-121">-Description</span></span>
<span data-ttu-id="eb955-122">Descrizione della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="eb955-122">The managed application definition description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb955-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="eb955-123">-DisplayName</span></span>
<span data-ttu-id="eb955-124">Nome visualizzato della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="eb955-124">The managed application definition display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb955-125">-ID</span><span class="sxs-lookup"><span data-stu-id="eb955-125">-Id</span></span>
<span data-ttu-id="eb955-126">ID di definizione dell'applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="eb955-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="eb955-127">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb955-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb955-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb955-128">-Name</span></span>
<span data-ttu-id="eb955-129">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="eb955-129">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb955-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="eb955-130">-PackageFileUri</span></span>
<span data-ttu-id="eb955-131">URI del file del pacchetto di definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="eb955-131">The managed application definition package file uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb955-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="eb955-132">-Pre</span></span>
<span data-ttu-id="eb955-133">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="eb955-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb955-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb955-134">-ResourceGroupName</span></span>
<span data-ttu-id="eb955-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eb955-135">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb955-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="eb955-136">-Tag</span></span>
<span data-ttu-id="eb955-137">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="eb955-137">A hash table which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb955-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eb955-138">-Confirm</span></span>
<span data-ttu-id="eb955-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb955-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb955-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb955-140">-WhatIf</span></span>
<span data-ttu-id="eb955-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb955-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb955-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb955-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb955-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb955-143">CommonParameters</span></span>
<span data-ttu-id="eb955-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb955-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb955-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb955-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb955-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb955-146">INPUTS</span></span>

### <span data-ttu-id="eb955-147">System. String</span><span class="sxs-lookup"><span data-stu-id="eb955-147">System.String</span></span>
<span data-ttu-id="eb955-148">System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="eb955-148">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="eb955-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb955-149">OUTPUTS</span></span>

### <span data-ttu-id="eb955-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="eb955-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="eb955-151">Note</span><span class="sxs-lookup"><span data-stu-id="eb955-151">NOTES</span></span>

## <span data-ttu-id="eb955-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb955-152">RELATED LINKS</span></span>
