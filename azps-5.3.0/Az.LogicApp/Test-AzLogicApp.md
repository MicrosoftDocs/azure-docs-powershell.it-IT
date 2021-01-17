---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: d38363d27253bea023e837e9b84076ccdcbf2b8d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386116"
---
# <span data-ttu-id="b993f-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b993f-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="b993f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b993f-102">SYNOPSIS</span></span>
<span data-ttu-id="b993f-103">Convalida una definizione di app logica.</span><span class="sxs-lookup"><span data-stu-id="b993f-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="b993f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b993f-104">SYNTAX</span></span>

### <span data-ttu-id="b993f-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b993f-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b993f-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="b993f-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b993f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b993f-107">DESCRIPTION</span></span>
<span data-ttu-id="b993f-108">Il cmdlet **test-AzLogicApp** convalida una definizione di app logica in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b993f-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="b993f-109">Specificare il nome dell'app logica, il nome del gruppo di risorse, la posizione, lo stato, l'ID account di integrazione o i parametri.</span><span class="sxs-lookup"><span data-stu-id="b993f-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="b993f-110">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="b993f-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b993f-111">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="b993f-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b993f-112">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="b993f-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b993f-113">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="b993f-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b993f-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b993f-114">EXAMPLES</span></span>

### <span data-ttu-id="b993f-115">Esempio 1: convalidare un'app logica usando i percorsi di file</span><span class="sxs-lookup"><span data-stu-id="b993f-115">Example 1: Validate a logic app by using file paths</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="b993f-116">Questo comando Convalida un'app logica denominata LogicApp01 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b993f-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="b993f-117">Il comando specifica i percorsi dei file di definizione e parametri.</span><span class="sxs-lookup"><span data-stu-id="b993f-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="b993f-118">Esempio 2: convalidare un'app logica usando gli oggetti</span><span class="sxs-lookup"><span data-stu-id="b993f-118">Example 2: Validate a logic app by using objects</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="b993f-119">Questo comando Convalida un'app logica denominata LogicApp01 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b993f-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="b993f-120">Il comando specifica gli oggetti Definition e Parameter.</span><span class="sxs-lookup"><span data-stu-id="b993f-120">The command specifies definition and parameter objects.</span></span>

### <span data-ttu-id="b993f-121">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b993f-121">Example 3</span></span>

<span data-ttu-id="b993f-122">Convalida una definizione di app logica.</span><span class="sxs-lookup"><span data-stu-id="b993f-122">Validates a logic app definition.</span></span> <span data-ttu-id="b993f-123">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="b993f-123">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Test-AzLogicApp -DefinitionFilePath 'd:\workflows\Definition.json' -IntegrationAccountId <String> -Location 'westus' -Name 'LogicApp01' -ParameterFilePath 'd:\workflows\Parameters.json' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="b993f-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b993f-124">PARAMETERS</span></span>

### <span data-ttu-id="b993f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b993f-125">-DefaultProfile</span></span>
<span data-ttu-id="b993f-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b993f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b993f-127">-Definizione</span><span class="sxs-lookup"><span data-stu-id="b993f-127">-Definition</span></span>
<span data-ttu-id="b993f-128">Specifica la definizione di un'app logica come oggetto o stringa in formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="b993f-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="b993f-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="b993f-129">-DefinitionFilePath</span></span>
<span data-ttu-id="b993f-130">Specifica la definizione dell'app logica come percorso di un file di definizione in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="b993f-130">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="b993f-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="b993f-131">-IntegrationAccountId</span></span>
<span data-ttu-id="b993f-132">Specifica un ID account di integrazione per l'app logica.</span><span class="sxs-lookup"><span data-stu-id="b993f-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="b993f-133">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b993f-133">-Location</span></span>
<span data-ttu-id="b993f-134">Specifica la posizione dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="b993f-134">Specifies the location of the logic app.</span></span>
<span data-ttu-id="b993f-135">Immettere una posizione nel centro dati di Azure, ad esempio ovest degli Stati Uniti o Asia sud-orientale.</span><span class="sxs-lookup"><span data-stu-id="b993f-135">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="b993f-136">Puoi inserire un'app logica in qualsiasi posizione.</span><span class="sxs-lookup"><span data-stu-id="b993f-136">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="b993f-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="b993f-137">-Name</span></span>
<span data-ttu-id="b993f-138">Specifica il nome dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="b993f-138">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="b993f-139">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="b993f-139">-ParameterFilePath</span></span>
<span data-ttu-id="b993f-140">Specifica il percorso di un file di parametro formattato JSON.</span><span class="sxs-lookup"><span data-stu-id="b993f-140">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="b993f-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="b993f-141">-Parameters</span></span>
<span data-ttu-id="b993f-142">Specifica un oggetto raccolta Parameters dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="b993f-142">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="b993f-143">Specificare una tabella hash, un dizionario \<string\> o un dizionario \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="b993f-143">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="b993f-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b993f-144">-ResourceGroupName</span></span>
<span data-ttu-id="b993f-145">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b993f-145">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b993f-146">-Stato</span><span class="sxs-lookup"><span data-stu-id="b993f-146">-State</span></span>
<span data-ttu-id="b993f-147">Specifica lo stato dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="b993f-147">Specifies a state of the logic app.</span></span>
<span data-ttu-id="b993f-148">I valori accettabili per questo parametro sono: Enabled e disabled.</span><span class="sxs-lookup"><span data-stu-id="b993f-148">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="b993f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b993f-149">CommonParameters</span></span>
<span data-ttu-id="b993f-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b993f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b993f-151">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b993f-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b993f-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b993f-152">INPUTS</span></span>

### <span data-ttu-id="b993f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="b993f-153">System.String</span></span>

## <span data-ttu-id="b993f-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b993f-154">OUTPUTS</span></span>

### <span data-ttu-id="b993f-155">System. void</span><span class="sxs-lookup"><span data-stu-id="b993f-155">System.Void</span></span>

## <span data-ttu-id="b993f-156">Note</span><span class="sxs-lookup"><span data-stu-id="b993f-156">NOTES</span></span>

## <span data-ttu-id="b993f-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b993f-157">RELATED LINKS</span></span>

[<span data-ttu-id="b993f-158">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b993f-158">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="b993f-159">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b993f-159">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="b993f-160">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b993f-160">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="b993f-161">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b993f-161">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="b993f-162">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="b993f-162">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


