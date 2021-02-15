---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 34f09ca41326b2f6686a41cdeba0910317bc7a2c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182095"
---
# <span data-ttu-id="1571f-101">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="1571f-101">Start-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="1571f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1571f-102">SYNOPSIS</span></span>
<span data-ttu-id="1571f-103">Compila una configurazione DSC in Automazione.</span><span class="sxs-lookup"><span data-stu-id="1571f-103">Compiles a DSC configuration in Automation.</span></span>

## <span data-ttu-id="1571f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1571f-104">SYNTAX</span></span>

```
Start-AzAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1571f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1571f-105">DESCRIPTION</span></span>
<span data-ttu-id="1571f-106">Il cmdlet **Start-AzAutomationDscCompilationJob** compila una configurazione DSC (Desired State Configuration) APS nell'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1571f-106">The **Start-AzAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="1571f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1571f-107">EXAMPLES</span></span>

### <span data-ttu-id="1571f-108">Esempio 1: Compilare una configurazione di Azure DSC in Automazione</span><span class="sxs-lookup"><span data-stu-id="1571f-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1571f-109">Il primo comando crea un dizionario di parametri e li archivia nella $Params variabile.</span><span class="sxs-lookup"><span data-stu-id="1571f-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="1571f-110">Il secondo comando compila la configurazione DSC denominata Config01.</span><span class="sxs-lookup"><span data-stu-id="1571f-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="1571f-111">Il comando include i valori in $Params per i parametri di configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="1571f-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="1571f-112">Esempio 2: Compilare una configurazione DSC di Azure in Automazione con una nuova versione della build Node Configuration.</span><span class="sxs-lookup"><span data-stu-id="1571f-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="1571f-113">Come nel primo esempio, il primo comando crea un dizionario di parametri e li archivia nella $Params variabile.</span><span class="sxs-lookup"><span data-stu-id="1571f-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="1571f-114">Il secondo comando compila la configurazione DSC denominata Config01.</span><span class="sxs-lookup"><span data-stu-id="1571f-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="1571f-115">Il comando include i valori in $Params per i parametri di configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="1571f-115">The command includes the values in $Params for DSC configuration parameters.</span></span>
<span data-ttu-id="1571f-116">Non sostituisce la precedente Configurazione nodo esistente creando una nuova configurazione nodo con il nome Configurazione01[<2 <NodeName>>].</span><span class="sxs-lookup"><span data-stu-id="1571f-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="1571f-117">Il numero di versione viene incrementato in base al numero di versione esistente già presente.</span><span class="sxs-lookup"><span data-stu-id="1571f-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="1571f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1571f-118">PARAMETERS</span></span>

### <span data-ttu-id="1571f-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1571f-119">-AutomationAccountName</span></span>
<span data-ttu-id="1571f-120">Specifica il nome dell'account di automazione che contiene la configurazione DSC compilata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1571f-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1571f-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="1571f-121">-ConfigurationData</span></span>
<span data-ttu-id="1571f-122">Specifica un dizionario dei dati di configurazione per la configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="1571f-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1571f-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="1571f-123">-ConfigurationName</span></span>
<span data-ttu-id="1571f-124">Specifica il nome della configurazione DSC compilata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1571f-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1571f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1571f-125">-DefaultProfile</span></span>
<span data-ttu-id="1571f-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="1571f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1571f-127">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="1571f-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="1571f-128">Crea una nuova versione della build Node Configuration.</span><span class="sxs-lookup"><span data-stu-id="1571f-128">Creates a new Node Configuration build version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1571f-129">-Parameters</span><span class="sxs-lookup"><span data-stu-id="1571f-129">-Parameters</span></span>
<span data-ttu-id="1571f-130">Specifica un dizionario di parametri che questo cmdlet usa per compilare la configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="1571f-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1571f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1571f-131">-ResourceGroupName</span></span>
<span data-ttu-id="1571f-132">Specifica il nome di un gruppo di risorse in cui questo cmdlet compila una configurazione.</span><span class="sxs-lookup"><span data-stu-id="1571f-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1571f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1571f-133">-Confirm</span></span>
<span data-ttu-id="1571f-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1571f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1571f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1571f-135">-WhatIf</span></span>
<span data-ttu-id="1571f-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1571f-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1571f-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1571f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1571f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1571f-138">CommonParameters</span></span>
<span data-ttu-id="1571f-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1571f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1571f-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1571f-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1571f-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="1571f-141">INPUTS</span></span>

### <span data-ttu-id="1571f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1571f-142">System.String</span></span>

## <span data-ttu-id="1571f-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1571f-143">OUTPUTS</span></span>

### <span data-ttu-id="1571f-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="1571f-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="1571f-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="1571f-145">NOTES</span></span>

## <span data-ttu-id="1571f-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1571f-146">RELATED LINKS</span></span>

[<span data-ttu-id="1571f-147">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="1571f-147">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="1571f-148">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="1571f-148">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)


