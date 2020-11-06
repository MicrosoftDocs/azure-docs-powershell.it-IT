---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
ms.openlocfilehash: fa848a8249fa01a61a7aa50855f24b2813b9fdf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522113"
---
# <span data-ttu-id="b7ea0-101">Test-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="b7ea0-101">Test-AzureRmLogicApp</span></span>

## <span data-ttu-id="b7ea0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7ea0-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ea0-103">Convalida una definizione di app logica.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-103">Validates a logic app definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7ea0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7ea0-104">SYNTAX</span></span>

### <span data-ttu-id="b7ea0-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7ea0-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7ea0-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7ea0-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7ea0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7ea0-107">DESCRIPTION</span></span>
<span data-ttu-id="b7ea0-108">Il cmdlet **test-AzureRmLogicApp** convalida una definizione di app logica in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-108">The **Test-AzureRmLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="b7ea0-109">Specificare il nome dell'app logica, il nome del gruppo di risorse, la posizione, lo stato, l'ID account di integrazione o i parametri.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>

<span data-ttu-id="b7ea0-110">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b7ea0-111">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b7ea0-112">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b7ea0-113">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b7ea0-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7ea0-114">EXAMPLES</span></span>

### <span data-ttu-id="b7ea0-115">Esempio 1: convalidare un'app logica usando i percorsi di file</span><span class="sxs-lookup"><span data-stu-id="b7ea0-115">Example 1: Validate a logic app by using file paths</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="b7ea0-116">Questo comando Convalida un'app logica denominata LogicApp01 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="b7ea0-117">Il comando specifica i percorsi dei file di definizione e parametri.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="b7ea0-118">Esempio 2: convalidare un'app logica usando gli oggetti</span><span class="sxs-lookup"><span data-stu-id="b7ea0-118">Example 2: Validate a logic app by using objects</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="b7ea0-119">Questo comando Convalida un'app logica denominata LogicApp01 nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="b7ea0-120">Il comando specifica gli oggetti Definition e Parameter.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-120">The command specifies definition and parameter objects.</span></span>

## <span data-ttu-id="b7ea0-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7ea0-121">PARAMETERS</span></span>

### <span data-ttu-id="b7ea0-122">-Definizione</span><span class="sxs-lookup"><span data-stu-id="b7ea0-122">-Definition</span></span>
<span data-ttu-id="b7ea0-123">Specifica la definizione di un'app logica come oggetto o stringa in formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="b7ea0-123">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="b7ea0-124">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="b7ea0-124">-DefinitionFilePath</span></span>
<span data-ttu-id="b7ea0-125">Specifica la definizione dell'app logica come percorso di un file di definizione in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-125">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="b7ea0-126">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="b7ea0-126">-IntegrationAccountId</span></span>
<span data-ttu-id="b7ea0-127">Specifica un ID account di integrazione per l'app logica.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-127">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="b7ea0-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b7ea0-128">-Location</span></span>
<span data-ttu-id="b7ea0-129">Specifica la posizione dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-129">Specifies the location of the logic app.</span></span>
<span data-ttu-id="b7ea0-130">Immettere una posizione nel centro dati di Azure, ad esempio ovest degli Stati Uniti o Asia sud-orientale.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-130">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="b7ea0-131">Puoi inserire un'app logica in qualsiasi posizione.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-131">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="b7ea0-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7ea0-132">-Name</span></span>
<span data-ttu-id="b7ea0-133">Specifica il nome dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-133">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="b7ea0-134">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="b7ea0-134">-ParameterFilePath</span></span>
<span data-ttu-id="b7ea0-135">Specifica il percorso di un file di parametro formattato JSON.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-135">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="b7ea0-136">-Parameters</span><span class="sxs-lookup"><span data-stu-id="b7ea0-136">-Parameters</span></span>
<span data-ttu-id="b7ea0-137">Specifica un oggetto raccolta Parameters dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-137">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="b7ea0-138">Specificare una tabella hash, un dizionario \<string\> o un dizionario \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="b7ea0-138">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="b7ea0-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ea0-139">-ResourceGroupName</span></span>
<span data-ttu-id="b7ea0-140">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-140">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b7ea0-141">-Stato</span><span class="sxs-lookup"><span data-stu-id="b7ea0-141">-State</span></span>
<span data-ttu-id="b7ea0-142">Specifica lo stato dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-142">Specifies a state of the logic app.</span></span>
<span data-ttu-id="b7ea0-143">I valori accettabili per questo parametro sono: Enabled e disabled.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-143">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="b7ea0-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ea0-144">-DefaultProfile</span></span>
<span data-ttu-id="b7ea0-145">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7ea0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ea0-146">CommonParameters</span></span>
<span data-ttu-id="b7ea0-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ea0-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7ea0-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ea0-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7ea0-149">INPUTS</span></span>

## <span data-ttu-id="b7ea0-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7ea0-150">OUTPUTS</span></span>

### <span data-ttu-id="b7ea0-151">System. Object</span><span class="sxs-lookup"><span data-stu-id="b7ea0-151">System.Object</span></span>

## <span data-ttu-id="b7ea0-152">Note</span><span class="sxs-lookup"><span data-stu-id="b7ea0-152">NOTES</span></span>

## <span data-ttu-id="b7ea0-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7ea0-153">RELATED LINKS</span></span>

[<span data-ttu-id="b7ea0-154">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="b7ea0-154">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="b7ea0-155">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="b7ea0-155">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="b7ea0-156">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="b7ea0-156">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="b7ea0-157">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="b7ea0-157">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="b7ea0-158">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="b7ea0-158">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


