---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 49cd2fdb2d482621ea52f1df88c9bcd95521badd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519768"
---
# <span data-ttu-id="a71c4-101">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a71c4-101">Import-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="a71c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a71c4-102">SYNOPSIS</span></span>
<span data-ttu-id="a71c4-103">Importa un documento MOF come configurazione di nodi DSC in automazione.</span><span class="sxs-lookup"><span data-stu-id="a71c4-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a71c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a71c4-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a71c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a71c4-105">DESCRIPTION</span></span>
<span data-ttu-id="a71c4-106">Il cmdlet **Import-AzureRmAutomationDscConfiguration** importa un documento di configurazione MOF (Managed Object Format) in Azure Automation come configurazione di nodo di configurazione di stato desiderata (DSC).</span><span class="sxs-lookup"><span data-stu-id="a71c4-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="a71c4-107">Specificare il percorso di un file con estensione MOF.</span><span class="sxs-lookup"><span data-stu-id="a71c4-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="a71c4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a71c4-108">EXAMPLES</span></span>

### <span data-ttu-id="a71c4-109">Esempio 1: importare una configurazione di nodi DSC in automazione</span><span class="sxs-lookup"><span data-stu-id="a71c4-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="a71c4-110">Questo comando importa una configurazione del nodo DSC dal file denominato WebServer. mof nell'account di automazione denominato Contoso17, sotto la configurazione DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a71c4-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="a71c4-111">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="a71c4-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a71c4-112">Se esiste una configurazione di nodo DSC esistente denominata ContosoConfiguration. webserver, questo comando lo sostituisce.</span><span class="sxs-lookup"><span data-stu-id="a71c4-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="a71c4-113">Esempio 2: importare una configurazione del nodo DSC in automazione e creare una nuova versione di compilazione e non sovrascrivere NodeConfiguration esistenti.</span><span class="sxs-lookup"><span data-stu-id="a71c4-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="a71c4-114">Questo comando importa una configurazione del nodo DSC dal file denominato WebServer. mof nell'account di automazione denominato Contoso17, sotto la configurazione DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a71c4-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="a71c4-115">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="a71c4-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a71c4-116">Se esiste una configurazione di nodo DSC esistente denominata ContosoConfiguration. webserver, questo comando aggiunge una nuova versione di compilazione con il nome ContosoConfiguration [2]. webserver.</span><span class="sxs-lookup"><span data-stu-id="a71c4-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="a71c4-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a71c4-117">PARAMETERS</span></span>

### <span data-ttu-id="a71c4-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a71c4-118">-AutomationAccountName</span></span>
<span data-ttu-id="a71c4-119">Specifica il nome dell'account di automazione in cui questo cmdlet importa una configurazione di nodi DSC.</span><span class="sxs-lookup"><span data-stu-id="a71c4-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="a71c4-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a71c4-120">-ConfigurationName</span></span>
<span data-ttu-id="a71c4-121">Specifica il nome di una configurazione DSC in automazione da usare come spazio dei nomi e contenitore per la configurazione del nodo da importare.</span><span class="sxs-lookup"><span data-stu-id="a71c4-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

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

### <span data-ttu-id="a71c4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a71c4-122">-DefaultProfile</span></span>
<span data-ttu-id="a71c4-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a71c4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a71c4-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a71c4-124">-Force</span></span>
<span data-ttu-id="a71c4-125">Indica che questo cmdlet sostituisce una configurazione di nodi DSC esistente nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="a71c4-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="a71c4-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="a71c4-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="a71c4-127">Crea una nuova versione di build di configurazione dei nodi.</span><span class="sxs-lookup"><span data-stu-id="a71c4-127">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="a71c4-128">-Path</span><span class="sxs-lookup"><span data-stu-id="a71c4-128">-Path</span></span>
<span data-ttu-id="a71c4-129">Specifica il percorso del documento di configurazione MOF importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a71c4-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

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

### <span data-ttu-id="a71c4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a71c4-130">-ResourceGroupName</span></span>
<span data-ttu-id="a71c4-131">Specifica il nome di un gruppo di risorse per cui questo cmdlet importa una configurazione di nodi DSC.</span><span class="sxs-lookup"><span data-stu-id="a71c4-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="a71c4-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a71c4-132">-Confirm</span></span>
<span data-ttu-id="a71c4-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a71c4-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71c4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a71c4-134">-WhatIf</span></span>
<span data-ttu-id="a71c4-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a71c4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a71c4-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a71c4-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a71c4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a71c4-137">CommonParameters</span></span>
<span data-ttu-id="a71c4-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a71c4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a71c4-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a71c4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a71c4-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a71c4-140">INPUTS</span></span>

### <span data-ttu-id="a71c4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a71c4-141">System.String</span></span>

## <span data-ttu-id="a71c4-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a71c4-142">OUTPUTS</span></span>

### <span data-ttu-id="a71c4-143">Microsoft. Azure. Commands. Automation. Model. NodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a71c4-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="a71c4-144">Note</span><span class="sxs-lookup"><span data-stu-id="a71c4-144">NOTES</span></span>

## <span data-ttu-id="a71c4-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a71c4-145">RELATED LINKS</span></span>

[<span data-ttu-id="a71c4-146">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a71c4-146">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="a71c4-147">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a71c4-147">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)


