---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: 6639a397c97be35565d374279b2981fa2b1eabd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952366"
---
# <span data-ttu-id="60c59-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="60c59-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="60c59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60c59-102">SYNOPSIS</span></span>
<span data-ttu-id="60c59-103">Convalida una definizione dell'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="60c59-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="60c59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60c59-104">SYNTAX</span></span>

### <span data-ttu-id="60c59-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="60c59-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60c59-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="60c59-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60c59-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="60c59-107">DESCRIPTION</span></span>
<span data-ttu-id="60c59-108">Il **cmdlet Test-AzLogicApp** convalida una definizione dell'app per la logica in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60c59-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="60c59-109">Specificare il nome dell'app per la logica, il nome del gruppo di risorse, la posizione, lo stato, l'ID account di integrazione o i parametri.</span><span class="sxs-lookup"><span data-stu-id="60c59-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="60c59-110">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="60c59-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="60c59-111">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="60c59-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="60c59-112">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="60c59-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="60c59-113">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="60c59-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="60c59-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60c59-114">EXAMPLES</span></span>

### <span data-ttu-id="60c59-115">Esempio 1: Convalidare un'app per la logica usando i percorsi di file</span><span class="sxs-lookup"><span data-stu-id="60c59-115">Example 1: Validate a logic app by using file paths</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="60c59-116">Questo comando convalida un'app per la logica denominata LogicApp01 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="60c59-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="60c59-117">Il comando specifica i percorsi dei file di definizione e dei parametri.</span><span class="sxs-lookup"><span data-stu-id="60c59-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="60c59-118">Esempio 2: Convalidare un'app per la logica usando oggetti</span><span class="sxs-lookup"><span data-stu-id="60c59-118">Example 2: Validate a logic app by using objects</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="60c59-119">Questo comando convalida un'app per la logica denominata LogicApp01 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="60c59-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="60c59-120">Il comando specifica gli oggetti definizione e parametro.</span><span class="sxs-lookup"><span data-stu-id="60c59-120">The command specifies definition and parameter objects.</span></span>

### <span data-ttu-id="60c59-121">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="60c59-121">Example 3</span></span>

<span data-ttu-id="60c59-122">Convalida una definizione dell'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="60c59-122">Validates a logic app definition.</span></span> <span data-ttu-id="60c59-123">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="60c59-123">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Test-AzLogicApp -DefinitionFilePath 'd:\workflows\Definition.json' -IntegrationAccountId <String> -Location 'westus' -Name 'LogicApp01' -ParameterFilePath 'd:\workflows\Parameters.json' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="60c59-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60c59-124">PARAMETERS</span></span>

### <span data-ttu-id="60c59-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60c59-125">-DefaultProfile</span></span>
<span data-ttu-id="60c59-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="60c59-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60c59-127">-Definition</span><span class="sxs-lookup"><span data-stu-id="60c59-127">-Definition</span></span>
<span data-ttu-id="60c59-128">Specifica la definizione di un'app per la logica come oggetto o stringa in formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="60c59-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c59-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="60c59-129">-DefinitionFilePath</span></span>
<span data-ttu-id="60c59-130">Specifica la definizione dell'app per la logica come percorso di un file di definizione in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="60c59-130">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c59-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="60c59-131">-IntegrationAccountId</span></span>
<span data-ttu-id="60c59-132">Specifica un ID account di integrazione per l'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="60c59-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="60c59-133">-Location</span><span class="sxs-lookup"><span data-stu-id="60c59-133">-Location</span></span>
<span data-ttu-id="60c59-134">Specifica la posizione dell'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="60c59-134">Specifies the location of the logic app.</span></span>
<span data-ttu-id="60c59-135">Immettere la posizione di un data center di Azure, ad esempio Stati Uniti occidentali o Asia sud-orientale.</span><span class="sxs-lookup"><span data-stu-id="60c59-135">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="60c59-136">È possibile inserire un'app per la logica in qualsiasi posizione.</span><span class="sxs-lookup"><span data-stu-id="60c59-136">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="60c59-137">-Name</span><span class="sxs-lookup"><span data-stu-id="60c59-137">-Name</span></span>
<span data-ttu-id="60c59-138">Specifica il nome dell'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="60c59-138">Specifies the name of the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60c59-139">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="60c59-139">-ParameterFilePath</span></span>
<span data-ttu-id="60c59-140">Specifica il percorso di un file di parametri in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="60c59-140">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="60c59-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="60c59-141">-Parameters</span></span>
<span data-ttu-id="60c59-142">Specifica un oggetto raccolta di parametri dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="60c59-142">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="60c59-143">Specificare una tabella hash, \<string\> un dizionario o un \<string, WorkflowParameter\> dizionario.</span><span class="sxs-lookup"><span data-stu-id="60c59-143">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c59-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60c59-144">-ResourceGroupName</span></span>
<span data-ttu-id="60c59-145">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60c59-145">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="60c59-146">-State</span><span class="sxs-lookup"><span data-stu-id="60c59-146">-State</span></span>
<span data-ttu-id="60c59-147">Specifica uno stato dell'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="60c59-147">Specifies a state of the logic app.</span></span>
<span data-ttu-id="60c59-148">I valori accettabili per questo parametro sono: Abilitato e Disabilitato.</span><span class="sxs-lookup"><span data-stu-id="60c59-148">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60c59-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60c59-149">CommonParameters</span></span>
<span data-ttu-id="60c59-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60c59-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60c59-151">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60c59-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60c59-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="60c59-152">INPUTS</span></span>

### <span data-ttu-id="60c59-153">System.String</span><span class="sxs-lookup"><span data-stu-id="60c59-153">System.String</span></span>

## <span data-ttu-id="60c59-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60c59-154">OUTPUTS</span></span>

### <span data-ttu-id="60c59-155">System.Void</span><span class="sxs-lookup"><span data-stu-id="60c59-155">System.Void</span></span>

## <span data-ttu-id="60c59-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="60c59-156">NOTES</span></span>

## <span data-ttu-id="60c59-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60c59-157">RELATED LINKS</span></span>

[<span data-ttu-id="60c59-158">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="60c59-158">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="60c59-159">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="60c59-159">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="60c59-160">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="60c59-160">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="60c59-161">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="60c59-161">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="60c59-162">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="60c59-162">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


