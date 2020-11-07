---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 9c860726993929a6618706037b5c53dff14a68ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687091"
---
# <span data-ttu-id="e270d-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="e270d-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="e270d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e270d-102">SYNOPSIS</span></span>
<span data-ttu-id="e270d-103">Crea una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e270d-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e270d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e270d-104">SYNTAX</span></span>

```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e270d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e270d-105">DESCRIPTION</span></span>
<span data-ttu-id="e270d-106">Il cmdlet **New-AzureRmPolicySetDefinition** crea una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e270d-106">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="e270d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e270d-107">EXAMPLES</span></span>

### <span data-ttu-id="e270d-108">Esempio 1: creare una definizione di set di criteri usando un file di set di criteri</span><span class="sxs-lookup"><span data-stu-id="e270d-108">Example 1: Create a policy set definition by using a policy set file</span></span>
```
PS C:\>New-AzureRmPolicySetDefinition -Name "VMPolicyDefinition" -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="e270d-109">Questo comando crea una definizione di set di criteri denominata VMPolicyDefinition che contiene le definizioni dei criteri specificate in C:\VMPolicy.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="e270d-109">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span>

## <span data-ttu-id="e270d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e270d-110">PARAMETERS</span></span>

### <span data-ttu-id="e270d-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e270d-111">-ApiVersion</span></span>
<span data-ttu-id="e270d-112">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="e270d-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e270d-113">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="e270d-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e270d-114">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="e270d-114">-Description</span></span>
<span data-ttu-id="e270d-115">Descrizione della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e270d-115">The description for policy set definition.</span></span>

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

### <span data-ttu-id="e270d-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e270d-116">-DisplayName</span></span>
<span data-ttu-id="e270d-117">Nome visualizzato per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e270d-117">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="e270d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e270d-118">-Name</span></span>
<span data-ttu-id="e270d-119">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e270d-119">The policy set definition name.</span></span>

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

### <span data-ttu-id="e270d-120">Parametro-</span><span class="sxs-lookup"><span data-stu-id="e270d-120">-Parameter</span></span>
<span data-ttu-id="e270d-121">Dichiarazione Parameters per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e270d-121">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="e270d-122">Può essere un percorso di un nome file contenente la dichiarazione parameters o la dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="e270d-122">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="e270d-123">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e270d-123">-PolicyDefinition</span></span>
<span data-ttu-id="e270d-124">Definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e270d-124">The policy set definition.</span></span> <span data-ttu-id="e270d-125">Può trattarsi di un percorso di un nome di file contenente le definizioni dei criteri oppure la definizione del set di criteri come stringa.</span><span class="sxs-lookup"><span data-stu-id="e270d-125">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="e270d-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="e270d-126">-Pre</span></span>
<span data-ttu-id="e270d-127">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="e270d-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e270d-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e270d-128">-Confirm</span></span>
<span data-ttu-id="e270d-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e270d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e270d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e270d-130">-DefaultProfile</span></span>
<span data-ttu-id="e270d-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e270d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e270d-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e270d-132">-Metadata</span></span>
<span data-ttu-id="e270d-133">Metadati per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="e270d-133">The metadata for policy set definition.</span></span> <span data-ttu-id="e270d-134">Può essere un percorso di un nome di file contenente i metadati oppure i metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="e270d-134">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="e270d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e270d-135">-WhatIf</span></span>
<span data-ttu-id="e270d-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e270d-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e270d-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e270d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e270d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e270d-138">CommonParameters</span></span>
<span data-ttu-id="e270d-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e270d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e270d-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e270d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e270d-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e270d-141">INPUTS</span></span>

### <span data-ttu-id="e270d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e270d-142">System.String</span></span>

## <span data-ttu-id="e270d-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e270d-143">OUTPUTS</span></span>

### <span data-ttu-id="e270d-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e270d-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e270d-145">Note</span><span class="sxs-lookup"><span data-stu-id="e270d-145">NOTES</span></span>

## <span data-ttu-id="e270d-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e270d-146">RELATED LINKS</span></span>

