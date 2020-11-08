---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplicationDefinition.md
ms.openlocfilehash: f676e8a56895017d89ef8f2843a647110143d05f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031120"
---
# <span data-ttu-id="0b600-101">New-AzManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="0b600-101">New-AzManagedApplicationDefinition</span></span>

## <span data-ttu-id="0b600-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b600-102">SYNOPSIS</span></span>
<span data-ttu-id="0b600-103">Crea una definizione di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="0b600-103">Creates a managed application definition.</span></span>

## <span data-ttu-id="0b600-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b600-104">SYNTAX</span></span>

```
New-AzManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b600-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b600-105">DESCRIPTION</span></span>
<span data-ttu-id="0b600-106">Il cmdlet **New-AzManagedApplicationDefinition** crea una definizione di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="0b600-106">The **New-AzManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="0b600-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b600-107">EXAMPLES</span></span>

### <span data-ttu-id="0b600-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0b600-108">Example 1</span></span>
```
PS> New-AzManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="0b600-109">Questo comando crea una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="0b600-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="0b600-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b600-110">PARAMETERS</span></span>

### <span data-ttu-id="0b600-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0b600-111">-ApiVersion</span></span>
<span data-ttu-id="0b600-112">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="0b600-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="0b600-113">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="0b600-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="0b600-114">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="0b600-114">-Authorization</span></span>
<span data-ttu-id="0b600-115">Autorizzazione per la definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="0b600-115">The managed application definition authorization.</span></span>
<span data-ttu-id="0b600-116">Coppie di autorizzazioni separate da virgola in un formato di \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="0b600-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="0b600-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="0b600-117">-CreateUiDefinition</span></span>
<span data-ttu-id="0b600-118">Definizione dell'interfaccia utente creata per la definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="0b600-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="0b600-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b600-119">-DefaultProfile</span></span>
<span data-ttu-id="0b600-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b600-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b600-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b600-121">-Description</span></span>
<span data-ttu-id="0b600-122">Descrizione della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="0b600-122">The managed application definition description.</span></span>

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

### <span data-ttu-id="0b600-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0b600-123">-DisplayName</span></span>
<span data-ttu-id="0b600-124">Nome visualizzato della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="0b600-124">The managed application definition display name.</span></span>

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

### <span data-ttu-id="0b600-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0b600-125">-Location</span></span>
<span data-ttu-id="0b600-126">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0b600-126">The resource location.</span></span>

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

### <span data-ttu-id="0b600-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="0b600-127">-LockLevel</span></span>
<span data-ttu-id="0b600-128">Livello del blocco per la definizione di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="0b600-128">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="0b600-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="0b600-129">-MainTemplate</span></span>
<span data-ttu-id="0b600-130">Modello principale della definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="0b600-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="0b600-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="0b600-131">-Name</span></span>
<span data-ttu-id="0b600-132">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="0b600-132">The managed application definition name.</span></span>

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

### <span data-ttu-id="0b600-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="0b600-133">-PackageFileUri</span></span>
<span data-ttu-id="0b600-134">URI del file del pacchetto di definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="0b600-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="0b600-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="0b600-135">-Pre</span></span>
<span data-ttu-id="0b600-136">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="0b600-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="0b600-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b600-137">-ResourceGroupName</span></span>
<span data-ttu-id="0b600-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0b600-138">The resource group name.</span></span>

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

### <span data-ttu-id="0b600-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b600-139">-Tag</span></span>
<span data-ttu-id="0b600-140">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="0b600-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="0b600-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0b600-141">-Confirm</span></span>
<span data-ttu-id="0b600-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b600-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b600-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b600-143">-WhatIf</span></span>
<span data-ttu-id="0b600-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b600-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b600-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b600-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b600-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b600-146">CommonParameters</span></span>
<span data-ttu-id="0b600-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b600-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b600-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b600-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b600-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b600-149">INPUTS</span></span>

### <span data-ttu-id="0b600-150">System. String</span><span class="sxs-lookup"><span data-stu-id="0b600-150">System.String</span></span>

### <span data-ttu-id="0b600-151">Microsoft. Azure. Commands. ResourceManager. Cmdlets. Entities. Application. ApplicationLockLevel</span><span class="sxs-lookup"><span data-stu-id="0b600-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel</span></span>

### <span data-ttu-id="0b600-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="0b600-152">System.String[]</span></span>

### <span data-ttu-id="0b600-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b600-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0b600-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b600-154">OUTPUTS</span></span>

### <span data-ttu-id="0b600-155">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0b600-155">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0b600-156">Note</span><span class="sxs-lookup"><span data-stu-id="0b600-156">NOTES</span></span>

## <span data-ttu-id="0b600-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b600-157">RELATED LINKS</span></span>
