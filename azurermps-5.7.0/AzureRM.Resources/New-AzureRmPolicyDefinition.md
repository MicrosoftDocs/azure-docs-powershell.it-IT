---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: e39d60863b9409a6d52f2f92dc312e98b8e50cf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512352"
---
# <span data-ttu-id="fe6bc-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fe6bc-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="fe6bc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe6bc-102">SYNOPSIS</span></span>
<span data-ttu-id="fe6bc-103">Crea una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe6bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe6bc-104">SYNTAX</span></span>

```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fe6bc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe6bc-105">DESCRIPTION</span></span>
<span data-ttu-id="fe6bc-106">Il cmdlet **New-AzureRmPolicyDefinition** crea una definizione di criteri che include una regola di criteri nel formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="fe6bc-106">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="fe6bc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe6bc-107">EXAMPLES</span></span>

### <span data-ttu-id="fe6bc-108">Esempio 1: creare una definizione di criteri usando un file di criteri</span><span class="sxs-lookup"><span data-stu-id="fe6bc-108">Example 1: Create a policy definition by using a policy file</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -Policy C:\VMPolicy.json
```

<span data-ttu-id="fe6bc-109">Questo comando crea una definizione di criteri denominata VMPolicyDefinition che contiene la regola di criteri specificata in C:\VMPolicy.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-109">This command creates a policy definition named VMPolicyDefinition that contains the policy rule specified in C:\VMPolicy.json.</span></span>

### <span data-ttu-id="fe6bc-110">Esempio 2: creare una definizione di criteri inline</span><span class="sxs-lookup"><span data-stu-id="fe6bc-110">Example 2: Create a policy definition inline</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -DisplayName "Virtual Machine policy definition" -Policy "{""if"":{""source"":""action"",""equals"":""Microsoft.Compute/virtualMachines/write""},""then"":{""effect"":""deny""}}"
```

<span data-ttu-id="fe6bc-111">Questo comando crea una definizione di criteri denominata VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-111">This command creates a policy definition named VMPolicyDefinition.</span></span>
<span data-ttu-id="fe6bc-112">Il comando specifica i criteri come stringa in un formato JSON valido.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-112">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="fe6bc-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe6bc-113">PARAMETERS</span></span>

### <span data-ttu-id="fe6bc-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fe6bc-114">-ApiVersion</span></span>
<span data-ttu-id="fe6bc-115">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="fe6bc-116">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="fe6bc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe6bc-117">-DefaultProfile</span></span>
<span data-ttu-id="fe6bc-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fe6bc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe6bc-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe6bc-119">-Description</span></span>
<span data-ttu-id="fe6bc-120">Specifica una descrizione per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-120">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="fe6bc-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fe6bc-121">-DisplayName</span></span>
<span data-ttu-id="fe6bc-122">Specifica un nome visualizzato per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-122">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="fe6bc-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fe6bc-123">-InformationAction</span></span>
<span data-ttu-id="fe6bc-124">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fe6bc-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fe6bc-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fe6bc-126">Continuare</span><span class="sxs-lookup"><span data-stu-id="fe6bc-126">Continue</span></span>
- <span data-ttu-id="fe6bc-127">Ignora</span><span class="sxs-lookup"><span data-stu-id="fe6bc-127">Ignore</span></span>
- <span data-ttu-id="fe6bc-128">Informarsi</span><span class="sxs-lookup"><span data-stu-id="fe6bc-128">Inquire</span></span>
- <span data-ttu-id="fe6bc-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fe6bc-129">SilentlyContinue</span></span>
- <span data-ttu-id="fe6bc-130">Stop</span><span class="sxs-lookup"><span data-stu-id="fe6bc-130">Stop</span></span>
- <span data-ttu-id="fe6bc-131">Sospensione</span><span class="sxs-lookup"><span data-stu-id="fe6bc-131">Suspend</span></span>

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

### <span data-ttu-id="fe6bc-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fe6bc-132">-InformationVariable</span></span>
<span data-ttu-id="fe6bc-133">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fe6bc-134">-Metadata</span><span class="sxs-lookup"><span data-stu-id="fe6bc-134">-Metadata</span></span>
<span data-ttu-id="fe6bc-135">Metadati per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-135">The metadata for policy definition.</span></span> <span data-ttu-id="fe6bc-136">Può essere un percorso di un nome di file contenente i metadati oppure i metadati come stringa</span><span class="sxs-lookup"><span data-stu-id="fe6bc-136">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="fe6bc-137">-Modalità</span><span class="sxs-lookup"><span data-stu-id="fe6bc-137">-Mode</span></span>
<span data-ttu-id="fe6bc-138">Modalità della definizione del criterio</span><span class="sxs-lookup"><span data-stu-id="fe6bc-138">The mode of the policy definition</span></span>

```yaml
Type: PolicyDefinitionMode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6bc-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe6bc-139">-Name</span></span>
<span data-ttu-id="fe6bc-140">Specifica un nome per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-140">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="fe6bc-141">Parametro-</span><span class="sxs-lookup"><span data-stu-id="fe6bc-141">-Parameter</span></span>
<span data-ttu-id="fe6bc-142">Dichiarazione Parameters per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-142">The parameters declaration for policy definition.</span></span> <span data-ttu-id="fe6bc-143">Può essere un percorso di un nome file contenente la dichiarazione parameters o la dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-143">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="fe6bc-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="fe6bc-144">-Policy</span></span>
<span data-ttu-id="fe6bc-145">Specifica una regola di criteri per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-145">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="fe6bc-146">Puoi specificare il percorso di un file con estensione JSON o una stringa che contiene il criterio in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-146">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="fe6bc-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="fe6bc-147">-Pre</span></span>
<span data-ttu-id="fe6bc-148">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="fe6bc-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe6bc-149">CommonParameters</span></span>
<span data-ttu-id="fe6bc-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe6bc-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe6bc-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe6bc-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe6bc-152">INPUTS</span></span>

### <span data-ttu-id="fe6bc-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fe6bc-153">None</span></span>
<span data-ttu-id="fe6bc-154">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="fe6bc-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe6bc-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe6bc-155">OUTPUTS</span></span>

### <span data-ttu-id="fe6bc-156">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fe6bc-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fe6bc-157">Note</span><span class="sxs-lookup"><span data-stu-id="fe6bc-157">NOTES</span></span>

## <span data-ttu-id="fe6bc-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe6bc-158">RELATED LINKS</span></span>

[<span data-ttu-id="fe6bc-159">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fe6bc-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="fe6bc-160">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fe6bc-160">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="fe6bc-161">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fe6bc-161">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


