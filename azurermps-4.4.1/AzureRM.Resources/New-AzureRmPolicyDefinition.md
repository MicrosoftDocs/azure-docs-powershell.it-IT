---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: 5140219c5392a7fb9c727998ae248d600edfde23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519982"
---
# <span data-ttu-id="d97aa-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d97aa-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="d97aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d97aa-102">SYNOPSIS</span></span>
<span data-ttu-id="d97aa-103">Crea una definizione di criteri.</span><span class="sxs-lookup"><span data-stu-id="d97aa-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d97aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d97aa-104">SYNTAX</span></span>

```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d97aa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d97aa-105">DESCRIPTION</span></span>
<span data-ttu-id="d97aa-106">Il cmdlet **New-AzureRmPolicyDefinition** crea una definizione di criteri che include una regola di criteri nel formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="d97aa-106">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="d97aa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d97aa-107">EXAMPLES</span></span>

### <span data-ttu-id="d97aa-108">Esempio 1: creare una definizione di criteri usando un file di criteri</span><span class="sxs-lookup"><span data-stu-id="d97aa-108">Example 1: Create a policy definition by using a policy file</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -Policy C:\VMPolicy.json
```

<span data-ttu-id="d97aa-109">Questo comando crea una definizione di criteri denominata VMPolicyDefinition che contiene la regola di criteri specificata in C:\VMPolicy.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="d97aa-109">This command creates a policy definition named VMPolicyDefinition that contains the policy rule specified in C:\VMPolicy.json.</span></span>

### <span data-ttu-id="d97aa-110">Esempio 2: creare una definizione di criteri inline</span><span class="sxs-lookup"><span data-stu-id="d97aa-110">Example 2: Create a policy definition inline</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -DisplayName "Virtual Machine policy definition" -Policy "{""if"":{""source"":""action"",""equals"":""Microsoft.Compute/virtualMachines/write""},""then"":{""effect"":""deny""}}"
```

<span data-ttu-id="d97aa-111">Questo comando crea una definizione di criteri denominata VMPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="d97aa-111">This command creates a policy definition named VMPolicyDefinition.</span></span>
<span data-ttu-id="d97aa-112">Il comando specifica i criteri come stringa in un formato JSON valido.</span><span class="sxs-lookup"><span data-stu-id="d97aa-112">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="d97aa-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d97aa-113">PARAMETERS</span></span>

### <span data-ttu-id="d97aa-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d97aa-114">-ApiVersion</span></span>
<span data-ttu-id="d97aa-115">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="d97aa-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d97aa-116">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="d97aa-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d97aa-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="d97aa-117">-Description</span></span>
<span data-ttu-id="d97aa-118">Specifica una descrizione per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d97aa-118">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="d97aa-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d97aa-119">-DisplayName</span></span>
<span data-ttu-id="d97aa-120">Specifica un nome visualizzato per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d97aa-120">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="d97aa-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d97aa-121">-InformationAction</span></span>
<span data-ttu-id="d97aa-122">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="d97aa-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d97aa-123">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d97aa-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d97aa-124">Continuare</span><span class="sxs-lookup"><span data-stu-id="d97aa-124">Continue</span></span>
- <span data-ttu-id="d97aa-125">Ignora</span><span class="sxs-lookup"><span data-stu-id="d97aa-125">Ignore</span></span>
- <span data-ttu-id="d97aa-126">Informarsi</span><span class="sxs-lookup"><span data-stu-id="d97aa-126">Inquire</span></span>
- <span data-ttu-id="d97aa-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d97aa-127">SilentlyContinue</span></span>
- <span data-ttu-id="d97aa-128">Stop</span><span class="sxs-lookup"><span data-stu-id="d97aa-128">Stop</span></span>
- <span data-ttu-id="d97aa-129">Sospensione</span><span class="sxs-lookup"><span data-stu-id="d97aa-129">Suspend</span></span>

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

### <span data-ttu-id="d97aa-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d97aa-130">-InformationVariable</span></span>
<span data-ttu-id="d97aa-131">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="d97aa-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d97aa-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="d97aa-132">-Name</span></span>
<span data-ttu-id="d97aa-133">Specifica un nome per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d97aa-133">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="d97aa-134">Parametro-</span><span class="sxs-lookup"><span data-stu-id="d97aa-134">-Parameter</span></span>
<span data-ttu-id="d97aa-135">Dichiarazione Parameters per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d97aa-135">The parameters declaration for policy definition.</span></span> <span data-ttu-id="d97aa-136">Può essere un percorso di un nome file contenente la dichiarazione parameters o la dichiarazione Parameters come stringa.</span><span class="sxs-lookup"><span data-stu-id="d97aa-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="d97aa-137">-Policy</span><span class="sxs-lookup"><span data-stu-id="d97aa-137">-Policy</span></span>
<span data-ttu-id="d97aa-138">Specifica una regola di criteri per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d97aa-138">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="d97aa-139">Puoi specificare il percorso di un file con estensione JSON o una stringa che contiene il criterio in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="d97aa-139">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="d97aa-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="d97aa-140">-Pre</span></span>
<span data-ttu-id="d97aa-141">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="d97aa-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d97aa-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d97aa-142">-DefaultProfile</span></span>
<span data-ttu-id="d97aa-143">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d97aa-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d97aa-144">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d97aa-144">-Metadata</span></span>
<span data-ttu-id="d97aa-145">Metadati per la definizione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="d97aa-145">The metadata for policy definition.</span></span> <span data-ttu-id="d97aa-146">Può essere un percorso di un nome di file contenente i metadati oppure i metadati come stringa.</span><span class="sxs-lookup"><span data-stu-id="d97aa-146">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="d97aa-147">-Modalità</span><span class="sxs-lookup"><span data-stu-id="d97aa-147">-Mode</span></span>
<span data-ttu-id="d97aa-148">Modalità della definizione del criterio.</span><span class="sxs-lookup"><span data-stu-id="d97aa-148">The mode of the policy definition.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d97aa-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d97aa-149">CommonParameters</span></span>
<span data-ttu-id="d97aa-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d97aa-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d97aa-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d97aa-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d97aa-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d97aa-152">INPUTS</span></span>

## <span data-ttu-id="d97aa-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d97aa-153">OUTPUTS</span></span>

### <span data-ttu-id="d97aa-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d97aa-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d97aa-155">Note</span><span class="sxs-lookup"><span data-stu-id="d97aa-155">NOTES</span></span>

## <span data-ttu-id="d97aa-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d97aa-156">RELATED LINKS</span></span>

[<span data-ttu-id="d97aa-157">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d97aa-157">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d97aa-158">Remove-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d97aa-158">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="d97aa-159">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d97aa-159">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


