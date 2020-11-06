---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
ms.openlocfilehash: ea36cf36b32df4c61c159e89cfdae12acdcc9509
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517999"
---
# <span data-ttu-id="c5fa0-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c5fa0-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="c5fa0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="c5fa0-103">Crea una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5fa0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5fa0-104">SYNTAX</span></span>

```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5fa0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5fa0-105">DESCRIPTION</span></span>
<span data-ttu-id="c5fa0-106">Il cmdlet **New-AzureRmPolicySetDefinition** crea una definizione di set di criteri.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-106">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="c5fa0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5fa0-107">EXAMPLES</span></span>

### <span data-ttu-id="c5fa0-108">Esempio 1: creare una definizione di set di criteri usando un file di set di criteri</span><span class="sxs-lookup"><span data-stu-id="c5fa0-108">Example 1: Create a policy set definition by using a policy set file</span></span>
```
PS C:\>New-AzureRmPolicySetDefinition -Name "VMPolicyDefinition" -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="c5fa0-109">Questo comando crea una definizione di set di criteri denominata VMPolicyDefinition che contiene le definizioni dei criteri specificate in C:\VMPolicy.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-109">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span>

## <span data-ttu-id="c5fa0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5fa0-110">PARAMETERS</span></span>

### <span data-ttu-id="c5fa0-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c5fa0-111">-ApiVersion</span></span>
<span data-ttu-id="c5fa0-112">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c5fa0-113">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c5fa0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5fa0-114">-DefaultProfile</span></span>
<span data-ttu-id="c5fa0-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c5fa0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5fa0-116">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5fa0-116">-Description</span></span>
<span data-ttu-id="c5fa0-117">Descrizione della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-117">The description for policy set definition.</span></span>

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

### <span data-ttu-id="c5fa0-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c5fa0-118">-DisplayName</span></span>
<span data-ttu-id="c5fa0-119">Nome visualizzato per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-119">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="c5fa0-120">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c5fa0-120">-Metadata</span></span>
<span data-ttu-id="c5fa0-121">Metadati per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-121">The metadata for policy set definition.</span></span> <span data-ttu-id="c5fa0-122">Può essere un percorso di un nome di file contenente i metadati oppure i metadati come stringa</span><span class="sxs-lookup"><span data-stu-id="c5fa0-122">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="c5fa0-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5fa0-123">-Name</span></span>
<span data-ttu-id="c5fa0-124">Nome della definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-124">The policy set definition name.</span></span>

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

### <span data-ttu-id="c5fa0-125">Parametro-</span><span class="sxs-lookup"><span data-stu-id="c5fa0-125">-Parameter</span></span>
<span data-ttu-id="c5fa0-126">Dichiarazione Parameters per la definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-126">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="c5fa0-127">Può essere un percorso di un nome file contenente la dichiarazione parameters o la dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-127">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="c5fa0-128">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c5fa0-128">-PolicyDefinition</span></span>
<span data-ttu-id="c5fa0-129">Definizione del set di criteri.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-129">The policy set definition.</span></span> <span data-ttu-id="c5fa0-130">Può trattarsi di un percorso di un nome di file contenente le definizioni dei criteri oppure la definizione del set di criteri come stringa.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-130">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="c5fa0-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="c5fa0-131">-Pre</span></span>
<span data-ttu-id="c5fa0-132">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c5fa0-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c5fa0-133">-Confirm</span></span>
<span data-ttu-id="c5fa0-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5fa0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5fa0-135">-WhatIf</span></span>
<span data-ttu-id="c5fa0-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5fa0-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5fa0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5fa0-138">CommonParameters</span></span>
<span data-ttu-id="c5fa0-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5fa0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5fa0-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5fa0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5fa0-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5fa0-141">INPUTS</span></span>

### <span data-ttu-id="c5fa0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c5fa0-142">System.String</span></span>

## <span data-ttu-id="c5fa0-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5fa0-143">OUTPUTS</span></span>

### <span data-ttu-id="c5fa0-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c5fa0-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c5fa0-145">Note</span><span class="sxs-lookup"><span data-stu-id="c5fa0-145">NOTES</span></span>

## <span data-ttu-id="c5fa0-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5fa0-146">RELATED LINKS</span></span>
