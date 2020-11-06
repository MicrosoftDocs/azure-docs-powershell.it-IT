---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyDefinition.md
ms.openlocfilehash: 63ab8e9004b993429af31cb54e360c0b6d9854fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520769"
---
# <span data-ttu-id="025f1-101">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="025f1-101">Get-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="025f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="025f1-102">SYNOPSIS</span></span>
<span data-ttu-id="025f1-103">Ottiene le definizioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="025f1-103">Gets policy definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="025f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="025f1-104">SYNTAX</span></span>

### <span data-ttu-id="025f1-105">Set di parametri di tutte le definizioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="025f1-105">The list all policy definitions parameter set.</span></span> <span data-ttu-id="025f1-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="025f1-106">(Default)</span></span>
```
Get-AzureRmPolicyDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="025f1-107">Set di parametri nome definizione criteri.</span><span class="sxs-lookup"><span data-stu-id="025f1-107">The policy definition name parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="025f1-108">Set di parametri ID definizione criteri.</span><span class="sxs-lookup"><span data-stu-id="025f1-108">The policy definition Id parameter set.</span></span>
```
Get-AzureRmPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="025f1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="025f1-109">DESCRIPTION</span></span>
<span data-ttu-id="025f1-110">Il cmdlet **Get-AzureRmPolicyDefinition** ottiene tutte le definizioni dei criteri o una specifica definizione di criteri identificata per nome o ID.</span><span class="sxs-lookup"><span data-stu-id="025f1-110">The **Get-AzureRmPolicyDefinition** cmdlet gets all the policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="025f1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="025f1-111">EXAMPLES</span></span>

### <span data-ttu-id="025f1-112">Esempio 1: ottenere tutte le definizioni dei criteri</span><span class="sxs-lookup"><span data-stu-id="025f1-112">Example 1: Get all policy definition</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition
```

<span data-ttu-id="025f1-113">Questo comando ottiene tutte le definizioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="025f1-113">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="025f1-114">Esempio 2: ottenere la definizione dei criteri per nome</span><span class="sxs-lookup"><span data-stu-id="025f1-114">Example 2: Get policy definition by name</span></span>
```
PS C:\>Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="025f1-115">Questo comando ottiene la definizione dei criteri denominata VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="025f1-115">This command gets the policy definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="025f1-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="025f1-116">PARAMETERS</span></span>

### <span data-ttu-id="025f1-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="025f1-117">-ApiVersion</span></span>
<span data-ttu-id="025f1-118">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="025f1-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="025f1-119">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="025f1-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="025f1-120">-ID</span><span class="sxs-lookup"><span data-stu-id="025f1-120">-Id</span></span>
<span data-ttu-id="025f1-121">Specifica l'ID risorsa completo per la definizione dei criteri ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="025f1-121">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="025f1-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="025f1-122">-InformationAction</span></span>
<span data-ttu-id="025f1-123">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="025f1-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="025f1-124">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="025f1-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="025f1-125">Continuare</span><span class="sxs-lookup"><span data-stu-id="025f1-125">Continue</span></span>
- <span data-ttu-id="025f1-126">Ignora</span><span class="sxs-lookup"><span data-stu-id="025f1-126">Ignore</span></span>
- <span data-ttu-id="025f1-127">Informarsi</span><span class="sxs-lookup"><span data-stu-id="025f1-127">Inquire</span></span>
- <span data-ttu-id="025f1-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="025f1-128">SilentlyContinue</span></span>
- <span data-ttu-id="025f1-129">Stop</span><span class="sxs-lookup"><span data-stu-id="025f1-129">Stop</span></span>
- <span data-ttu-id="025f1-130">Sospensione</span><span class="sxs-lookup"><span data-stu-id="025f1-130">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025f1-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="025f1-131">-InformationVariable</span></span>
<span data-ttu-id="025f1-132">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="025f1-132">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025f1-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="025f1-133">-Name</span></span>
<span data-ttu-id="025f1-134">Specifica il nome della definizione del criterio ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="025f1-134">Specifies the name of the policy definition that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="025f1-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="025f1-135">-Pre</span></span>
<span data-ttu-id="025f1-136">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="025f1-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="025f1-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025f1-137">-DefaultProfile</span></span>
<span data-ttu-id="025f1-138">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="025f1-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="025f1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025f1-139">CommonParameters</span></span>
<span data-ttu-id="025f1-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="025f1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025f1-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="025f1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025f1-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="025f1-142">INPUTS</span></span>

## <span data-ttu-id="025f1-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="025f1-143">OUTPUTS</span></span>

### <span data-ttu-id="025f1-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="025f1-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="025f1-145">Note</span><span class="sxs-lookup"><span data-stu-id="025f1-145">NOTES</span></span>

## <span data-ttu-id="025f1-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="025f1-146">RELATED LINKS</span></span>

[<span data-ttu-id="025f1-147">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="025f1-147">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="025f1-148">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="025f1-148">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="025f1-149">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="025f1-149">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


