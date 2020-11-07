---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 4a66541d870d30f2de199297417d211479ecc83b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521536"
---
# <span data-ttu-id="d9346-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="d9346-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="d9346-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9346-102">SYNOPSIS</span></span>
<span data-ttu-id="d9346-103">Crea una definizione di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="d9346-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9346-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9346-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9346-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9346-105">DESCRIPTION</span></span>
<span data-ttu-id="d9346-106">Il cmdlet **New-AzureRmManagedApplicationDefinition** crea una definizione di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="d9346-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="d9346-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9346-107">EXAMPLES</span></span>

### <span data-ttu-id="d9346-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d9346-108">Example 1</span></span>
```
PS C:\> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName "test" -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="d9346-109">Questo comando crea una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="d9346-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="d9346-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9346-110">PARAMETERS</span></span>

### <span data-ttu-id="d9346-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d9346-111">-ApiVersion</span></span>
<span data-ttu-id="d9346-112">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="d9346-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d9346-113">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="d9346-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d9346-114">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="d9346-114">-Authorization</span></span>
<span data-ttu-id="d9346-115">Autorizzazione per la definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="d9346-115">The managed application definition authorization.</span></span>
<span data-ttu-id="d9346-116">Coppie di autorizzazioni separate da virgola in un formato di \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="d9346-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

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

### <span data-ttu-id="d9346-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9346-117">-DefaultProfile</span></span>
<span data-ttu-id="d9346-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9346-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9346-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9346-119">-Description</span></span>
<span data-ttu-id="d9346-120">Descrizione della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="d9346-120">The managed application definition description.</span></span>

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

### <span data-ttu-id="d9346-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d9346-121">-DisplayName</span></span>
<span data-ttu-id="d9346-122">Nome visualizzato della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="d9346-122">The managed application definition display name.</span></span>

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

### <span data-ttu-id="d9346-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d9346-123">-Location</span></span>
<span data-ttu-id="d9346-124">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d9346-124">The resource location.</span></span>

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

### <span data-ttu-id="d9346-125">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="d9346-125">-LockLevel</span></span>
<span data-ttu-id="d9346-126">Livello del blocco per la definizione di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="d9346-126">The level of the lock for managed application definition.</span></span>

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

### <span data-ttu-id="d9346-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9346-127">-Name</span></span>
<span data-ttu-id="d9346-128">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="d9346-128">The managed application definition name.</span></span>

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

### <span data-ttu-id="d9346-129">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="d9346-129">-PackageFileUri</span></span>
<span data-ttu-id="d9346-130">URI del file del pacchetto di definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="d9346-130">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="d9346-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="d9346-131">-Pre</span></span>
<span data-ttu-id="d9346-132">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="d9346-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d9346-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9346-133">-ResourceGroupName</span></span>
<span data-ttu-id="d9346-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d9346-134">The resource group name.</span></span>

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

### <span data-ttu-id="d9346-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="d9346-135">-Tag</span></span>
<span data-ttu-id="d9346-136">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="d9346-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d9346-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d9346-137">-Confirm</span></span>
<span data-ttu-id="d9346-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9346-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9346-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9346-139">-WhatIf</span></span>
<span data-ttu-id="d9346-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9346-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9346-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d9346-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9346-142">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="d9346-142">-CreateUiDefinition</span></span>
<span data-ttu-id="d9346-143">La definizione dell'applicazione gestita crea la definizione dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="d9346-143">The managed application definition create ui definition.</span></span>

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

### <span data-ttu-id="d9346-144">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="d9346-144">-MainTemplate</span></span>
<span data-ttu-id="d9346-145">Modello principale della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="d9346-145">The managed application definition main template.</span></span>

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

### <span data-ttu-id="d9346-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9346-146">CommonParameters</span></span>
<span data-ttu-id="d9346-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9346-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9346-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9346-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9346-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9346-149">INPUTS</span></span>

### <span data-ttu-id="d9346-150">System. String</span><span class="sxs-lookup"><span data-stu-id="d9346-150">System.String</span></span>
<span data-ttu-id="d9346-151">Microsoft. Azure. Commands. ResourceManager. Cmdlets. Entities. Application. ApplicationLockLevel System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d9346-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="d9346-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9346-152">OUTPUTS</span></span>

### <span data-ttu-id="d9346-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d9346-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d9346-154">Note</span><span class="sxs-lookup"><span data-stu-id="d9346-154">NOTES</span></span>

## <span data-ttu-id="d9346-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9346-155">RELATED LINKS</span></span>
