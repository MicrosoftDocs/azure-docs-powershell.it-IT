---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 3036b02d280542ffa4c8eea85dafed2da8eb5e28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201102"
---
# <span data-ttu-id="d2c10-101">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2c10-101">Import-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="d2c10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2c10-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c10-103">Importa un documento MOF come configurazione nodo DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="d2c10-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

## <span data-ttu-id="d2c10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2c10-104">SYNTAX</span></span>

```
Import-AzAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2c10-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d2c10-105">DESCRIPTION</span></span>
<span data-ttu-id="d2c10-106">Il cmdlet **Import-AzAutomationDscConfiguration** importa un documento di configurazione MOF (Managed Object Format) in Automazione di Azure come configurazione del nodo DSC (Desired State Configuration).</span><span class="sxs-lookup"><span data-stu-id="d2c10-106">The **Import-AzAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="d2c10-107">Specificare il percorso di un file con estensione mof.</span><span class="sxs-lookup"><span data-stu-id="d2c10-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="d2c10-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2c10-108">EXAMPLES</span></span>

### <span data-ttu-id="d2c10-109">Esempio 1: Importare una configurazione nodo DSC nell'automazione</span><span class="sxs-lookup"><span data-stu-id="d2c10-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="d2c10-110">Questo comando importa una configurazione nodo DSC dal file denominato webserver.mof nell'account di automazione denominato Contoso17, nella configurazione DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d2c10-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="d2c10-111">Il comando specifica il *parametro Force.*</span><span class="sxs-lookup"><span data-stu-id="d2c10-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="d2c10-112">Se esiste una configurazione nodo DSC esistente denominata ContosoConfiguration.webserver, questo comando la sostituisce.</span><span class="sxs-lookup"><span data-stu-id="d2c10-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="d2c10-113">Esempio 2: importare una configurazione nodo DSC nell'automazione e creare una nuova versione della build e non sovrascrivere la nodeConfiguration esistente.</span><span class="sxs-lookup"><span data-stu-id="d2c10-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="d2c10-114">Questo comando importa una configurazione nodo DSC dal file denominato webserver.mof nell'account di automazione denominato Contoso17, nella configurazione DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d2c10-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="d2c10-115">Il comando specifica il *parametro Force.*</span><span class="sxs-lookup"><span data-stu-id="d2c10-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="d2c10-116">Se è presente una configurazione nodo DSC esistente denominata ContosoConfiguration.webserver, questo comando aggiunge una nuova versione di build con il nome ContosoConfiguration[2].webserver.</span><span class="sxs-lookup"><span data-stu-id="d2c10-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="d2c10-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2c10-117">PARAMETERS</span></span>

### <span data-ttu-id="d2c10-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d2c10-118">-AutomationAccountName</span></span>
<span data-ttu-id="d2c10-119">Specifica il nome dell'account di automazione in cui questo cmdlet importa una configurazione del nodo DSC.</span><span class="sxs-lookup"><span data-stu-id="d2c10-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="d2c10-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d2c10-120">-ConfigurationName</span></span>
<span data-ttu-id="d2c10-121">Specifica il nome di una configurazione DSC nell'automazione da usare come spazio dei nomi e contenitore per la configurazione del nodo da importare.</span><span class="sxs-lookup"><span data-stu-id="d2c10-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

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

### <span data-ttu-id="d2c10-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c10-122">-DefaultProfile</span></span>
<span data-ttu-id="d2c10-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d2c10-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2c10-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d2c10-124">-Force</span></span>
<span data-ttu-id="d2c10-125">Indica che questo cmdlet sostituisce la configurazione di un nodo DSC esistente nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="d2c10-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="d2c10-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="d2c10-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="d2c10-127">Crea una nuova versione della build Node Configuration.</span><span class="sxs-lookup"><span data-stu-id="d2c10-127">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="d2c10-128">-Path</span><span class="sxs-lookup"><span data-stu-id="d2c10-128">-Path</span></span>
<span data-ttu-id="d2c10-129">Specifica il percorso del documento di configurazione MOF importato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2c10-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

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

### <span data-ttu-id="d2c10-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2c10-130">-ResourceGroupName</span></span>
<span data-ttu-id="d2c10-131">Specifica il nome di un gruppo di risorse per cui questo cmdlet importa una configurazione del nodo DSC.</span><span class="sxs-lookup"><span data-stu-id="d2c10-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="d2c10-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2c10-132">-Confirm</span></span>
<span data-ttu-id="d2c10-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2c10-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2c10-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2c10-134">-WhatIf</span></span>
<span data-ttu-id="d2c10-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2c10-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2c10-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2c10-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2c10-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c10-137">CommonParameters</span></span>
<span data-ttu-id="d2c10-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2c10-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c10-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2c10-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c10-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="d2c10-140">INPUTS</span></span>

### <span data-ttu-id="d2c10-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d2c10-141">System.String</span></span>

## <span data-ttu-id="d2c10-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2c10-142">OUTPUTS</span></span>

### <span data-ttu-id="d2c10-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2c10-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="d2c10-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="d2c10-144">NOTES</span></span>

## <span data-ttu-id="d2c10-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2c10-145">RELATED LINKS</span></span>

[<span data-ttu-id="d2c10-146">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2c10-146">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="d2c10-147">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2c10-147">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)


