---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: 947cd0674e5fcd704b305b5963f3ed06e008f3fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971805"
---
# <span data-ttu-id="1f2d6-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="1f2d6-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="1f2d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f2d6-102">SYNOPSIS</span></span>
<span data-ttu-id="1f2d6-103">Crea una definizione di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="1f2d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f2d6-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f2d6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1f2d6-105">DESCRIPTION</span></span>
<span data-ttu-id="1f2d6-106">Il cmdlet **New-AzManagedApplicationDefinition crea** una definizione di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="1f2d6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f2d6-107">EXAMPLES</span></span>

### <span data-ttu-id="1f2d6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1f2d6-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="1f2d6-109">Questo comando crea una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="1f2d6-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="1f2d6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f2d6-110">PARAMETERS</span></span>

### <span data-ttu-id="1f2d6-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1f2d6-111">-ApiVersion</span></span>
<span data-ttu-id="1f2d6-112">Se impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1f2d6-113">Se non viene specificato, la versione dell'API viene automaticamente determinata come la più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1f2d6-114">-Authorization</span><span class="sxs-lookup"><span data-stu-id="1f2d6-114">-Authorization</span></span>
<span data-ttu-id="1f2d6-115">Autorizzazione di definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-115">The managed application definition authorization.</span></span>
<span data-ttu-id="1f2d6-116">Coppie di autorizzazione separate da virgole in un \<principalId\> formato:\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="1f2d6-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="1f2d6-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="1f2d6-117">-CreateUiDefinition</span></span>
<span data-ttu-id="1f2d6-118">Definizione di interfaccia utente creata dalla definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="1f2d6-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="1f2d6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f2d6-119">-DefaultProfile</span></span>
<span data-ttu-id="1f2d6-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f2d6-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f2d6-121">-Description</span></span>
<span data-ttu-id="1f2d6-122">Descrizione della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="1f2d6-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1f2d6-123">-DisplayName</span></span>
<span data-ttu-id="1f2d6-124">Nome visualizzato della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="1f2d6-125">-Location</span><span class="sxs-lookup"><span data-stu-id="1f2d6-125">-Location</span></span>
<span data-ttu-id="1f2d6-126">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-126">The resource location.</span></span>

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

### <span data-ttu-id="1f2d6-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="1f2d6-127">-LockLevel</span></span>
<span data-ttu-id="1f2d6-128">Livello del blocco per la definizione di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="1f2d6-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="1f2d6-129">-MainTemplate</span></span>
<span data-ttu-id="1f2d6-130">Modello principale di definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="1f2d6-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="1f2d6-131">-Name</span><span class="sxs-lookup"><span data-stu-id="1f2d6-131">-Name</span></span>
<span data-ttu-id="1f2d6-132">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="1f2d6-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="1f2d6-133">-PackageFileUri</span></span>
<span data-ttu-id="1f2d6-134">URI del file del pacchetto della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="1f2d6-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="1f2d6-135">-Pre</span></span>
<span data-ttu-id="1f2d6-136">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1f2d6-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f2d6-137">-ResourceGroupName</span></span>
<span data-ttu-id="1f2d6-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-138">The resource group name.</span></span>

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

### <span data-ttu-id="1f2d6-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f2d6-139">-Tag</span></span>
<span data-ttu-id="1f2d6-140">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1f2d6-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f2d6-141">-Confirm</span></span>
<span data-ttu-id="1f2d6-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f2d6-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f2d6-143">-WhatIf</span></span>
<span data-ttu-id="1f2d6-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f2d6-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f2d6-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f2d6-146">CommonParameters</span></span>
<span data-ttu-id="1f2d6-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f2d6-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1f2d6-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f2d6-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="1f2d6-149">INPUTS</span></span>

### <span data-ttu-id="1f2d6-150">System.String</span><span class="sxs-lookup"><span data-stu-id="1f2d6-150">System.String</span></span>

### <span data-ttu-id="1f2d6-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="1f2d6-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="1f2d6-152">System.String[]</span><span class="sxs-lookup"><span data-stu-id="1f2d6-152">System.String[]</span></span>

### <span data-ttu-id="1f2d6-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1f2d6-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1f2d6-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f2d6-154">OUTPUTS</span></span>

### <span data-ttu-id="1f2d6-155">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="1f2d6-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1f2d6-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="1f2d6-156">NOTES</span></span>

## <span data-ttu-id="1f2d6-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f2d6-157">RELATED LINKS</span></span>
