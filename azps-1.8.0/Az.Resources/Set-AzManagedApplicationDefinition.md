---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplicationDefinition.md
ms.openlocfilehash: d1da0ce7f8a88a12b0714960a60d5b2aa523a0a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677275"
---
# <span data-ttu-id="755c8-101">Set-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="755c8-101">Set-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="755c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="755c8-102">SYNOPSIS</span></span>
<span data-ttu-id="755c8-103">Definizione dell'applicazione gestita degli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="755c8-103">Updates managed application definition</span></span>

## <span data-ttu-id="755c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="755c8-104">SYNTAX</span></span>

### <span data-ttu-id="755c8-105">SetByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="755c8-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="755c8-106">SetById</span><span class="sxs-lookup"><span data-stu-id="755c8-106">SetById</span></span>
```
Set-AzManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="755c8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="755c8-107">DESCRIPTION</span></span>
<span data-ttu-id="755c8-108">Il cmdlet **set-AzManagedApplicationDefinition** aggiorna le definizioni delle applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="755c8-108">The **Set-AzManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="755c8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="755c8-109">EXAMPLES</span></span>

### <span data-ttu-id="755c8-110">Esempio 1: aggiornare la descrizione della definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="755c8-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="755c8-111">Questo comando Aggiorna la descrizione della definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="755c8-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="755c8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="755c8-112">PARAMETERS</span></span>

### <span data-ttu-id="755c8-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="755c8-113">-ApiVersion</span></span>
<span data-ttu-id="755c8-114">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="755c8-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="755c8-115">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="755c8-115">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755c8-116">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="755c8-116">-Authorization</span></span>
<span data-ttu-id="755c8-117">Autorizzazione per la definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="755c8-117">The managed application definition authorization.</span></span>
<span data-ttu-id="755c8-118">Coppie di autorizzazioni separate da virgola in un formato di \< PrincipalId \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="755c8-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="755c8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="755c8-119">-DefaultProfile</span></span>
<span data-ttu-id="755c8-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="755c8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="755c8-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="755c8-121">-Description</span></span>
<span data-ttu-id="755c8-122">Descrizione della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="755c8-122">The managed application definition description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="755c8-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="755c8-123">-DisplayName</span></span>
<span data-ttu-id="755c8-124">Nome visualizzato della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="755c8-124">The managed application definition display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="755c8-125">-ID</span><span class="sxs-lookup"><span data-stu-id="755c8-125">-Id</span></span>
<span data-ttu-id="755c8-126">ID di definizione dell'applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="755c8-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="755c8-127">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="755c8-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="755c8-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="755c8-128">-Name</span></span>
<span data-ttu-id="755c8-129">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="755c8-129">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="755c8-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="755c8-130">-PackageFileUri</span></span>
<span data-ttu-id="755c8-131">URI del file del pacchetto di definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="755c8-131">The managed application definition package file uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="755c8-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="755c8-132">-Pre</span></span>
<span data-ttu-id="755c8-133">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="755c8-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="755c8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="755c8-134">-ResourceGroupName</span></span>
<span data-ttu-id="755c8-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="755c8-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="755c8-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="755c8-136">-Tag</span></span>
<span data-ttu-id="755c8-137">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="755c8-137">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="755c8-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="755c8-138">-Confirm</span></span>
<span data-ttu-id="755c8-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="755c8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="755c8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="755c8-140">-WhatIf</span></span>
<span data-ttu-id="755c8-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="755c8-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="755c8-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="755c8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="755c8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="755c8-143">CommonParameters</span></span>
<span data-ttu-id="755c8-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="755c8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="755c8-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="755c8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="755c8-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="755c8-146">INPUTS</span></span>

### <span data-ttu-id="755c8-147">System. String</span><span class="sxs-lookup"><span data-stu-id="755c8-147">System.String</span></span>

### <span data-ttu-id="755c8-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="755c8-148">System.String[]</span></span>

### <span data-ttu-id="755c8-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="755c8-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="755c8-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="755c8-150">OUTPUTS</span></span>

### <span data-ttu-id="755c8-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="755c8-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="755c8-152">Note</span><span class="sxs-lookup"><span data-stu-id="755c8-152">NOTES</span></span>

## <span data-ttu-id="755c8-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="755c8-153">RELATED LINKS</span></span>
