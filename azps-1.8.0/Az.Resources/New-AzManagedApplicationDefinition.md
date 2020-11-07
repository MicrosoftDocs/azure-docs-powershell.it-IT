---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: 1c59b6aba1a839086bb923556c86e3b93b80365a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677350"
---
# <span data-ttu-id="78c0e-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="78c0e-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="78c0e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="78c0e-103">Crea una definizione di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="78c0e-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="78c0e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78c0e-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78c0e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78c0e-105">DESCRIPTION</span></span>
<span data-ttu-id="78c0e-106">Il cmdlet **New-AzManagedApplicationDefinition** crea una definizione di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="78c0e-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="78c0e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78c0e-107">EXAMPLES</span></span>

### <span data-ttu-id="78c0e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="78c0e-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="78c0e-109">Questo comando crea una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="78c0e-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="78c0e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78c0e-110">PARAMETERS</span></span>

### <span data-ttu-id="78c0e-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="78c0e-111">-ApiVersion</span></span>
<span data-ttu-id="78c0e-112">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="78c0e-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="78c0e-113">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="78c0e-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="78c0e-114">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="78c0e-114">-Authorization</span></span>
<span data-ttu-id="78c0e-115">Autorizzazione per la definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="78c0e-115">The managed application definition authorization.</span></span>
<span data-ttu-id="78c0e-116">Coppie di autorizzazioni separate da virgola in un formato di \< PrincipalId \> : \< roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="78c0e-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c0e-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="78c0e-117">-CreateUiDefinition</span></span>
<span data-ttu-id="78c0e-118">Definizione dell'interfaccia utente creata per la definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="78c0e-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="78c0e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78c0e-119">-DefaultProfile</span></span>
<span data-ttu-id="78c0e-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78c0e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78c0e-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="78c0e-121">-Description</span></span>
<span data-ttu-id="78c0e-122">Descrizione della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="78c0e-122">The managed application definition description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c0e-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="78c0e-123">-DisplayName</span></span>
<span data-ttu-id="78c0e-124">Nome visualizzato della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="78c0e-124">The managed application definition display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c0e-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="78c0e-125">-Location</span></span>
<span data-ttu-id="78c0e-126">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="78c0e-126">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78c0e-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="78c0e-127">-LockLevel</span></span>
<span data-ttu-id="78c0e-128">Livello del blocco per la definizione di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="78c0e-128">The level of the lock for managed application definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c0e-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="78c0e-129">-MainTemplate</span></span>
<span data-ttu-id="78c0e-130">Modello principale della definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="78c0e-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="78c0e-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="78c0e-131">-Name</span></span>
<span data-ttu-id="78c0e-132">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="78c0e-132">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c0e-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="78c0e-133">-PackageFileUri</span></span>
<span data-ttu-id="78c0e-134">URI del file del pacchetto di definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="78c0e-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="78c0e-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="78c0e-135">-Pre</span></span>
<span data-ttu-id="78c0e-136">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="78c0e-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="78c0e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78c0e-137">-ResourceGroupName</span></span>
<span data-ttu-id="78c0e-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="78c0e-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78c0e-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="78c0e-139">-Tag</span></span>
<span data-ttu-id="78c0e-140">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="78c0e-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="78c0e-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="78c0e-141">-Confirm</span></span>
<span data-ttu-id="78c0e-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78c0e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78c0e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78c0e-143">-WhatIf</span></span>
<span data-ttu-id="78c0e-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78c0e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78c0e-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="78c0e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78c0e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c0e-146">CommonParameters</span></span>
<span data-ttu-id="78c0e-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78c0e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c0e-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78c0e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c0e-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78c0e-149">INPUTS</span></span>

### <span data-ttu-id="78c0e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="78c0e-150">System.String</span></span>

### <span data-ttu-id="78c0e-151">Microsoft. Azure. Commands. ResourceManager. Cmdlets. Entities. Application. ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="78c0e-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="78c0e-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="78c0e-152">System.String[]</span></span>

### <span data-ttu-id="78c0e-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="78c0e-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="78c0e-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78c0e-154">OUTPUTS</span></span>

### <span data-ttu-id="78c0e-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="78c0e-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="78c0e-156">Note</span><span class="sxs-lookup"><span data-stu-id="78c0e-156">NOTES</span></span>

## <span data-ttu-id="78c0e-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78c0e-157">RELATED LINKS</span></span>
