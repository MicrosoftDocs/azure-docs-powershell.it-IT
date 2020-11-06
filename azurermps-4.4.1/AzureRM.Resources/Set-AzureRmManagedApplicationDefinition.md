---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 4dc41f7510789664b5c453285ebea032c24f3ac7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510343"
---
# <span data-ttu-id="913bd-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="913bd-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="913bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="913bd-102">SYNOPSIS</span></span>
<span data-ttu-id="913bd-103">Definizione dell'applicazione gestita degli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="913bd-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="913bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="913bd-104">SYNTAX</span></span>

### <span data-ttu-id="913bd-105">Set di parametri del nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="913bd-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="913bd-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="913bd-106">(Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="913bd-107">Set di parametri ID definizione applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="913bd-107">The managed application definition Id parameter set.</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="913bd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="913bd-108">DESCRIPTION</span></span>
<span data-ttu-id="913bd-109">Il cmdlet **set-AzureRmManagedApplicationDefinition** aggiorna le definizioni delle applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="913bd-109">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="913bd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="913bd-110">EXAMPLES</span></span>

### <span data-ttu-id="913bd-111">Esempio 1: aggiornare la descrizione della definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="913bd-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="913bd-112">Questo comando Aggiorna la descrizione della definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="913bd-112">This command updates the managed application definition description</span></span>

## <span data-ttu-id="913bd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="913bd-113">PARAMETERS</span></span>

### <span data-ttu-id="913bd-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="913bd-114">-ApiVersion</span></span>
<span data-ttu-id="913bd-115">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="913bd-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="913bd-116">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="913bd-116">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="913bd-117">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="913bd-117">-Authorization</span></span>
<span data-ttu-id="913bd-118">Autorizzazione per la definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="913bd-118">The managed application definition authorization.</span></span>
<span data-ttu-id="913bd-119">Coppie di autorizzazioni separate da virgola in un formato di \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="913bd-119">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="913bd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913bd-120">-DefaultProfile</span></span>
<span data-ttu-id="913bd-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="913bd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913bd-122">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="913bd-122">-Description</span></span>
<span data-ttu-id="913bd-123">Descrizione della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="913bd-123">The managed application definition description.</span></span>

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

### <span data-ttu-id="913bd-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="913bd-124">-DisplayName</span></span>
<span data-ttu-id="913bd-125">Nome visualizzato della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="913bd-125">The managed application definition display name.</span></span>

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

### <span data-ttu-id="913bd-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="913bd-126">-Name</span></span>
<span data-ttu-id="913bd-127">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="913bd-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="913bd-128">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="913bd-128">-PackageFileUri</span></span>
<span data-ttu-id="913bd-129">URI del file del pacchetto di definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="913bd-129">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="913bd-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="913bd-130">-Pre</span></span>
<span data-ttu-id="913bd-131">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="913bd-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="913bd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="913bd-132">-ResourceGroupName</span></span>
<span data-ttu-id="913bd-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="913bd-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="913bd-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="913bd-134">-Tag</span></span>
<span data-ttu-id="913bd-135">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="913bd-135">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="913bd-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="913bd-136">-Confirm</span></span>
<span data-ttu-id="913bd-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="913bd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="913bd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="913bd-138">-WhatIf</span></span>
<span data-ttu-id="913bd-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="913bd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="913bd-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="913bd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="913bd-141">-ID</span><span class="sxs-lookup"><span data-stu-id="913bd-141">-Id</span></span>
<span data-ttu-id="913bd-142">ID di definizione dell'applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="913bd-142">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="913bd-143">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="913bd-143">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="913bd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913bd-144">CommonParameters</span></span>
<span data-ttu-id="913bd-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="913bd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913bd-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="913bd-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913bd-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="913bd-147">INPUTS</span></span>

### <span data-ttu-id="913bd-148">System. String</span><span class="sxs-lookup"><span data-stu-id="913bd-148">System.String</span></span>
<span data-ttu-id="913bd-149">System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="913bd-149">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="913bd-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="913bd-150">OUTPUTS</span></span>

### <span data-ttu-id="913bd-151">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="913bd-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="913bd-152">Note</span><span class="sxs-lookup"><span data-stu-id="913bd-152">NOTES</span></span>

## <span data-ttu-id="913bd-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="913bd-153">RELATED LINKS</span></span>

