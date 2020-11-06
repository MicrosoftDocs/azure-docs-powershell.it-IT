---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: d9d79374e426c6d895fbfcef957da20ed9721f70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519873"
---
# <span data-ttu-id="7c7a6-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7c7a6-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="7c7a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c7a6-102">SYNOPSIS</span></span>
<span data-ttu-id="7c7a6-103">Ottiene le definizioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c7a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c7a6-104">SYNTAX</span></span>

### <span data-ttu-id="7c7a6-105">GetAllPolicyDefinitions (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c7a6-105">GetAllPolicyDefinitions (Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7c7a6-106">GetByPolicyDefintionName</span><span class="sxs-lookup"><span data-stu-id="7c7a6-106">GetByPolicyDefintionName</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7c7a6-107">GetByPolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7c7a6-107">GetByPolicyDefinitionId</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7c7a6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c7a6-108">DESCRIPTION</span></span>
<span data-ttu-id="7c7a6-109">Il cmdlet **Get-AzureRmPolicyDefinition** ottiene tutte le definizioni dei criteri o una specifica definizione di criteri identificata per nome o ID.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-109">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="7c7a6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c7a6-110">EXAMPLES</span></span>

### <span data-ttu-id="7c7a6-111">Esempio 1: ottenere tutte le definizioni dei criteri</span><span class="sxs-lookup"><span data-stu-id="7c7a6-111">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="7c7a6-112">Questo comando ottiene tutte le definizioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-112">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="7c7a6-113">Esempio 2: ottenere la definizione dei criteri per nome</span><span class="sxs-lookup"><span data-stu-id="7c7a6-113">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="7c7a6-114">Questo comando ottiene la definizione dei criteri denominata VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-114">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="7c7a6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c7a6-115">PARAMETERS</span></span>

### <span data-ttu-id="7c7a6-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7c7a6-116">-ApiVersion</span></span>
<span data-ttu-id="7c7a6-117">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7c7a6-118">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7c7a6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c7a6-119">-DefaultProfile</span></span>
<span data-ttu-id="7c7a6-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7c7a6-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c7a6-121">-ID</span><span class="sxs-lookup"><span data-stu-id="7c7a6-121">-Id</span></span>
<span data-ttu-id="7c7a6-122">Specifica l'ID risorsa completo per la definizione dei criteri ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-122">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c7a6-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7c7a6-123">-InformationAction</span></span>
<span data-ttu-id="7c7a6-124">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7c7a6-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7c7a6-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7c7a6-126">Continuare</span><span class="sxs-lookup"><span data-stu-id="7c7a6-126">Continue</span></span>
- <span data-ttu-id="7c7a6-127">Ignora</span><span class="sxs-lookup"><span data-stu-id="7c7a6-127">Ignore</span></span>
- <span data-ttu-id="7c7a6-128">Informarsi</span><span class="sxs-lookup"><span data-stu-id="7c7a6-128">Inquire</span></span>
- <span data-ttu-id="7c7a6-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7c7a6-129">SilentlyContinue</span></span>
- <span data-ttu-id="7c7a6-130">Stop</span><span class="sxs-lookup"><span data-stu-id="7c7a6-130">Stop</span></span>
- <span data-ttu-id="7c7a6-131">Sospensione</span><span class="sxs-lookup"><span data-stu-id="7c7a6-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c7a6-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7c7a6-132">-InformationVariable</span></span>
<span data-ttu-id="7c7a6-133">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c7a6-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c7a6-134">-Name</span></span>
<span data-ttu-id="7c7a6-135">Specifica il nome della definizione del criterio ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-135">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetByPolicyDefintionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c7a6-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="7c7a6-136">-Pre</span></span>
<span data-ttu-id="7c7a6-137">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7c7a6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c7a6-138">CommonParameters</span></span>
<span data-ttu-id="7c7a6-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c7a6-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c7a6-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c7a6-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c7a6-141">INPUTS</span></span>

### <span data-ttu-id="7c7a6-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7c7a6-142">None</span></span>
<span data-ttu-id="7c7a6-143">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7c7a6-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7c7a6-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c7a6-144">OUTPUTS</span></span>

### <span data-ttu-id="7c7a6-145">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7c7a6-145">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7c7a6-146">Note</span><span class="sxs-lookup"><span data-stu-id="7c7a6-146">NOTES</span></span>

## <span data-ttu-id="7c7a6-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c7a6-147">RELATED LINKS</span></span>

[<span data-ttu-id="7c7a6-148">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7c7a6-148">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="7c7a6-149">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7c7a6-149">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="7c7a6-150">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7c7a6-150">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


