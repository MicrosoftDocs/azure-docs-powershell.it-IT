---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: ba2d158257f4be0e0daac8de5dd77e906e0abedc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866008"
---
# <span data-ttu-id="9efc0-101">Set-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="9efc0-101">Set-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="9efc0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9efc0-102">SYNOPSIS</span></span>
<span data-ttu-id="9efc0-103">Definizione dell'applicazione gestita degli aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="9efc0-103">Updates managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9efc0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9efc0-104">SYNTAX</span></span>

### <span data-ttu-id="9efc0-105">SetByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9efc0-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-Description <String>] [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9efc0-106">SetById</span><span class="sxs-lookup"><span data-stu-id="9efc0-106">SetById</span></span>
```
Set-AzureRmManagedApplicationDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PackageFileUri <String>] [-Authorization <String[]>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9efc0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9efc0-107">DESCRIPTION</span></span>
<span data-ttu-id="9efc0-108">Il cmdlet **set-AzureRmManagedApplicationDefinition** aggiorna le definizioni delle applicazioni gestite</span><span class="sxs-lookup"><span data-stu-id="9efc0-108">The **Set-AzureRmManagedApplicationDefinition** cmdlet updates managed application definitions</span></span>

## <span data-ttu-id="9efc0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9efc0-109">EXAMPLES</span></span>

### <span data-ttu-id="9efc0-110">Esempio 1: aggiornare la descrizione della definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="9efc0-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplicationDefinition -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applicationDefinitions/myAppDef" -Description "Updated description here"
```

<span data-ttu-id="9efc0-111">Questo comando Aggiorna la descrizione della definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="9efc0-111">This command updates the managed application definition description</span></span>

## <span data-ttu-id="9efc0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9efc0-112">PARAMETERS</span></span>

### <span data-ttu-id="9efc0-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9efc0-113">-ApiVersion</span></span>
<span data-ttu-id="9efc0-114">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="9efc0-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="9efc0-115">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="9efc0-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="9efc0-116">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="9efc0-116">-Authorization</span></span>
<span data-ttu-id="9efc0-117">Autorizzazione per la definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="9efc0-117">The managed application definition authorization.</span></span>
<span data-ttu-id="9efc0-118">Coppie di autorizzazioni separate da virgola in un formato di \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="9efc0-118">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="9efc0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9efc0-119">-DefaultProfile</span></span>
<span data-ttu-id="9efc0-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9efc0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9efc0-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="9efc0-121">-Description</span></span>
<span data-ttu-id="9efc0-122">Descrizione della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="9efc0-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="9efc0-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9efc0-123">-DisplayName</span></span>
<span data-ttu-id="9efc0-124">Nome visualizzato della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="9efc0-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="9efc0-125">-ID</span><span class="sxs-lookup"><span data-stu-id="9efc0-125">-Id</span></span>
<span data-ttu-id="9efc0-126">ID di definizione dell'applicazione gestita completo, incluso l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="9efc0-126">The fully qualified managed application definition Id, including the subscription.</span></span> <span data-ttu-id="9efc0-127">ad esempio/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9efc0-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

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

### <span data-ttu-id="9efc0-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="9efc0-128">-Name</span></span>
<span data-ttu-id="9efc0-129">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="9efc0-129">The managed application definition name.</span></span>

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

### <span data-ttu-id="9efc0-130">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="9efc0-130">-PackageFileUri</span></span>
<span data-ttu-id="9efc0-131">URI del file del pacchetto di definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="9efc0-131">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="9efc0-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="9efc0-132">-Pre</span></span>
<span data-ttu-id="9efc0-133">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="9efc0-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9efc0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9efc0-134">-ResourceGroupName</span></span>
<span data-ttu-id="9efc0-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9efc0-135">The resource group name.</span></span>

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

### <span data-ttu-id="9efc0-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="9efc0-136">-Tag</span></span>
<span data-ttu-id="9efc0-137">Tabella hash che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="9efc0-137">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="9efc0-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9efc0-138">-Confirm</span></span>
<span data-ttu-id="9efc0-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9efc0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9efc0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9efc0-140">-WhatIf</span></span>
<span data-ttu-id="9efc0-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9efc0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9efc0-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9efc0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9efc0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9efc0-143">CommonParameters</span></span>
<span data-ttu-id="9efc0-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9efc0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9efc0-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9efc0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9efc0-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9efc0-146">INPUTS</span></span>

### <span data-ttu-id="9efc0-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9efc0-147">System.String</span></span>
<span data-ttu-id="9efc0-148">System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9efc0-148">System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="9efc0-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9efc0-149">OUTPUTS</span></span>

### <span data-ttu-id="9efc0-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9efc0-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9efc0-151">Note</span><span class="sxs-lookup"><span data-stu-id="9efc0-151">NOTES</span></span>

## <span data-ttu-id="9efc0-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9efc0-152">RELATED LINKS</span></span>
