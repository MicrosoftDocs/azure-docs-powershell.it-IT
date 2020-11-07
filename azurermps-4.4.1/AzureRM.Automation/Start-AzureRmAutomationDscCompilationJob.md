---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 6e4db8baaa4e86fe9557ce20f1fd486ce14bdd6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686238"
---
# <span data-ttu-id="a14fb-101">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="a14fb-101">Start-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="a14fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a14fb-102">SYNOPSIS</span></span>
<span data-ttu-id="a14fb-103">Compila una configurazione DSC in automazione.</span><span class="sxs-lookup"><span data-stu-id="a14fb-103">Compiles a DSC configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a14fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a14fb-104">SYNTAX</span></span>

```
Start-AzureRmAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a14fb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a14fb-105">DESCRIPTION</span></span>
<span data-ttu-id="a14fb-106">Il cmdlet **Start-AzureRmAutomationDscCompilationJob** compila una configurazione DSC (APS desired state Configuration) in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a14fb-106">The **Start-AzureRmAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="a14fb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a14fb-107">EXAMPLES</span></span>

### <span data-ttu-id="a14fb-108">Esempio 1: compilare una configurazione di Azure DSC in automazione</span><span class="sxs-lookup"><span data-stu-id="a14fb-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzureRmAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a14fb-109">Il primo comando crea un dizionario di parametri e li archivia nella variabile $Params.</span><span class="sxs-lookup"><span data-stu-id="a14fb-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="a14fb-110">Il secondo comando Compila la configurazione DSC denominata Config01.</span><span class="sxs-lookup"><span data-stu-id="a14fb-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="a14fb-111">Il comando include i valori in $Params per i parametri di configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="a14fb-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="a14fb-112">Esempio 2: compilare una configurazione di Azure DSC in automazione con una nuova versione di build di configurazione dei nodi.</span><span class="sxs-lookup"><span data-stu-id="a14fb-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzureRmAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="a14fb-113">In modo simile al primo esempio, il primo comando crea un dizionario di parametri e li archivia nella variabile $Params.</span><span class="sxs-lookup"><span data-stu-id="a14fb-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="a14fb-114">Il secondo comando Compila la configurazione DSC denominata Config01.</span><span class="sxs-lookup"><span data-stu-id="a14fb-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="a14fb-115">Il comando include i valori in $Params per i parametri di configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="a14fb-115">The command includes the values in $Params for DSC configuration parameters.</span></span>

<span data-ttu-id="a14fb-116">Non esegue l'override della configurazione del nodo esistente precedente creando una nuova configurazione di nodo con il nome Config01 [<2>]. <NodeName> .</span><span class="sxs-lookup"><span data-stu-id="a14fb-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="a14fb-117">Il numero di versione viene incrementato in base al numero di versione esistente già presente.</span><span class="sxs-lookup"><span data-stu-id="a14fb-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="a14fb-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a14fb-118">PARAMETERS</span></span>

### <span data-ttu-id="a14fb-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a14fb-119">-AutomationAccountName</span></span>
<span data-ttu-id="a14fb-120">Specifica il nome dell'account di automazione che contiene la configurazione DSC che questo cmdlet compila.</span><span class="sxs-lookup"><span data-stu-id="a14fb-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="a14fb-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="a14fb-121">-ConfigurationData</span></span>
<span data-ttu-id="a14fb-122">Specifica un dizionario di dati di configurazione per la configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="a14fb-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

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

### <span data-ttu-id="a14fb-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a14fb-123">-ConfigurationName</span></span>
<span data-ttu-id="a14fb-124">Specifica il nome della configurazione DSC che questo cmdlet compila.</span><span class="sxs-lookup"><span data-stu-id="a14fb-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="a14fb-125">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="a14fb-125">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="a14fb-126">Crea una nuova versione di build di configurazione dei nodi.</span><span class="sxs-lookup"><span data-stu-id="a14fb-126">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="a14fb-127">-Parameters</span><span class="sxs-lookup"><span data-stu-id="a14fb-127">-Parameters</span></span>
<span data-ttu-id="a14fb-128">Specifica un dizionario di parametri usato da questo cmdlet per compilare la configurazione DSC.</span><span class="sxs-lookup"><span data-stu-id="a14fb-128">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

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

### <span data-ttu-id="a14fb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a14fb-129">-ResourceGroupName</span></span>
<span data-ttu-id="a14fb-130">Specifica il nome di un gruppo di risorse in cui questo cmdlet compila una configurazione.</span><span class="sxs-lookup"><span data-stu-id="a14fb-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="a14fb-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a14fb-131">-Confirm</span></span>
<span data-ttu-id="a14fb-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a14fb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a14fb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a14fb-133">-WhatIf</span></span>
<span data-ttu-id="a14fb-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a14fb-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a14fb-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a14fb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a14fb-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a14fb-136">-DefaultProfile</span></span>
<span data-ttu-id="a14fb-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a14fb-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a14fb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a14fb-138">CommonParameters</span></span>
<span data-ttu-id="a14fb-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a14fb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a14fb-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a14fb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a14fb-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a14fb-141">INPUTS</span></span>

## <span data-ttu-id="a14fb-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a14fb-142">OUTPUTS</span></span>

### <span data-ttu-id="a14fb-143">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="a14fb-143">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="a14fb-144">Note</span><span class="sxs-lookup"><span data-stu-id="a14fb-144">NOTES</span></span>

## <span data-ttu-id="a14fb-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a14fb-145">RELATED LINKS</span></span>

[<span data-ttu-id="a14fb-146">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="a14fb-146">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="a14fb-147">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="a14fb-147">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)


