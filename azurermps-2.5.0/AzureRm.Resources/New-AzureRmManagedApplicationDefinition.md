---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagedapplicationdefinition
schema: 2.0.0
ms.openlocfilehash: 3451a922af2b2af469b7edba1539f52cabb64eb2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866825"
---
# <span data-ttu-id="5a580-101">New-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="5a580-101">New-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="5a580-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a580-102">SYNOPSIS</span></span>
<span data-ttu-id="5a580-103">Crea una definizione di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="5a580-103">Creates a managed application definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a580-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a580-104">SYNTAX</span></span>

```
New-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> -DisplayName <String>
 -Description <String> -Location <String> -LockLevel <ApplicationLockLevel> [-PackageFileUri <String>]
 [-CreateUiDefinition <String>] [-MainTemplate <String>] -Authorization <String[]> [-Tag <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a580-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a580-105">DESCRIPTION</span></span>
<span data-ttu-id="5a580-106">Il cmdlet **New-AzureRmManagedApplicationDefinition** crea una definizione di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="5a580-106">The **New-AzureRmManagedApplicationDefinition** cmdlet creates a managed application definition.</span></span>

## <span data-ttu-id="5a580-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a580-107">EXAMPLES</span></span>

### <span data-ttu-id="5a580-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5a580-108">Example 1</span></span>
```
PS> New-AzureRmManagedApplicationDefinition -Name myAppDef -ResourceGroupName myRG -DisplayName test -Description "sample description" -Location westus -LockLevel ReadOnly -PackageFileUri https://sample.blob.core.windows.net/files/myPackage.zip -Authorization <principalId:roleDefinitionId>
```

<span data-ttu-id="5a580-109">Questo comando crea una definizione di applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="5a580-109">This command creates a managed application definition</span></span>

## <span data-ttu-id="5a580-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a580-110">PARAMETERS</span></span>

### <span data-ttu-id="5a580-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5a580-111">-ApiVersion</span></span>
<span data-ttu-id="5a580-112">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="5a580-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="5a580-113">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="5a580-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="5a580-114">-Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="5a580-114">-Authorization</span></span>
<span data-ttu-id="5a580-115">Autorizzazione per la definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="5a580-115">The managed application definition authorization.</span></span>
<span data-ttu-id="5a580-116">Coppie di autorizzazioni separate da virgola in un formato di \<principalId\> :\<roleDefinitionId\></span><span class="sxs-lookup"><span data-stu-id="5a580-116">Comma separated authorization pairs in a format of \<principalId\>:\<roleDefinitionId\></span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a580-117">-CreateUiDefinition</span><span class="sxs-lookup"><span data-stu-id="5a580-117">-CreateUiDefinition</span></span>
<span data-ttu-id="5a580-118">Definizione dell'interfaccia utente creata per la definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="5a580-118">The managed application definition create ui definition</span></span>

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

### <span data-ttu-id="5a580-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a580-119">-DefaultProfile</span></span>
<span data-ttu-id="5a580-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a580-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a580-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a580-121">-Description</span></span>
<span data-ttu-id="5a580-122">Descrizione della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="5a580-122">The managed application definition description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a580-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5a580-123">-DisplayName</span></span>
<span data-ttu-id="5a580-124">Nome visualizzato della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="5a580-124">The managed application definition display name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a580-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5a580-125">-Location</span></span>
<span data-ttu-id="5a580-126">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5a580-126">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a580-127">-LockLevel</span><span class="sxs-lookup"><span data-stu-id="5a580-127">-LockLevel</span></span>
<span data-ttu-id="5a580-128">Livello del blocco per la definizione di applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="5a580-128">The level of the lock for managed application definition.</span></span>

```yaml
Type: ApplicationLockLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, CanNotDelete, ReadOnly

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a580-129">-MainTemplate</span><span class="sxs-lookup"><span data-stu-id="5a580-129">-MainTemplate</span></span>
<span data-ttu-id="5a580-130">Modello principale della definizione dell'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="5a580-130">The managed application definition main template</span></span>

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

### <span data-ttu-id="5a580-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a580-131">-Name</span></span>
<span data-ttu-id="5a580-132">Nome della definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="5a580-132">The managed application definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a580-133">-PackageFileUri</span><span class="sxs-lookup"><span data-stu-id="5a580-133">-PackageFileUri</span></span>
<span data-ttu-id="5a580-134">URI del file del pacchetto di definizione dell'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="5a580-134">The managed application definition package file uri.</span></span>

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

### <span data-ttu-id="5a580-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="5a580-135">-Pre</span></span>
<span data-ttu-id="5a580-136">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="5a580-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5a580-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a580-137">-ResourceGroupName</span></span>
<span data-ttu-id="5a580-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5a580-138">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a580-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="5a580-139">-Tag</span></span>
<span data-ttu-id="5a580-140">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="5a580-140">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="5a580-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5a580-141">-Confirm</span></span>
<span data-ttu-id="5a580-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a580-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a580-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a580-143">-WhatIf</span></span>
<span data-ttu-id="5a580-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a580-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a580-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a580-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a580-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a580-146">CommonParameters</span></span>
<span data-ttu-id="5a580-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a580-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a580-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a580-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a580-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a580-149">INPUTS</span></span>

### <span data-ttu-id="5a580-150">System. String</span><span class="sxs-lookup"><span data-stu-id="5a580-150">System.String</span></span>
<span data-ttu-id="5a580-151">Microsoft. Azure. Commands. ResourceManager. Cmdlets. Entities. Application. ApplicationLockLevel System. String [] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5a580-151">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationLockLevel System.String[] System.Collections.Hashtable</span></span>

## <span data-ttu-id="5a580-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a580-152">OUTPUTS</span></span>

### <span data-ttu-id="5a580-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="5a580-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="5a580-154">Note</span><span class="sxs-lookup"><span data-stu-id="5a580-154">NOTES</span></span>

## <span data-ttu-id="5a580-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a580-155">RELATED LINKS</span></span>
