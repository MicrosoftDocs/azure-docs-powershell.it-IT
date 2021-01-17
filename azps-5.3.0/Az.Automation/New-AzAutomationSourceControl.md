---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: 17d1c7c94726543aa30a032423576c8a7dcb6fcc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478592"
---
# <span data-ttu-id="f6156-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="f6156-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="f6156-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6156-102">SYNOPSIS</span></span>
<span data-ttu-id="f6156-103">Crea un controllo origine di automazione.</span><span class="sxs-lookup"><span data-stu-id="f6156-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="f6156-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6156-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6156-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6156-105">DESCRIPTION</span></span>
<span data-ttu-id="f6156-106">Il cmdlet New-AzAutomationSourceControl crea una configurazione per collegare l'account di automazione di Azure con il mio VSTS TFVC, VST git o GitHub.</span><span class="sxs-lookup"><span data-stu-id="f6156-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="f6156-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6156-107">EXAMPLES</span></span>

### <span data-ttu-id="f6156-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f6156-108">Example 1</span></span>
<span data-ttu-id="f6156-109">Creare una configurazione del controllo del codice sorgente per collegare l'account di automazione di Azure con il progetto VSTS TFVC.</span><span class="sxs-lookup"><span data-stu-id="f6156-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="f6156-110">I progetti di TFVC non hanno rami e quindi il parametro Branch non è specificato.</span><span class="sxs-lookup"><span data-stu-id="f6156-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://contoso.visualstudio.com/ContosoProduction/_versionControl" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://contoso.visualstudio.com/ContosoProduc...
```

### <span data-ttu-id="f6156-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f6156-111">Example 2</span></span>
<span data-ttu-id="f6156-112">Creare una configurazione del controllo del codice sorgente per collegare l'account di automazione di Azure con il progetto Git di VSTS.</span><span class="sxs-lookup"><span data-stu-id="f6156-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://contoso.visualstudio.com/_git/Finance" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://contoso.visualstudio.com/_git/Finan...
```

### <span data-ttu-id="f6156-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f6156-113">Example 3</span></span>
<span data-ttu-id="f6156-114">Creare una configurazione del controllo del codice sorgente per collegare l'account di automazione di Azure con il mio progetto GitHub.</span><span class="sxs-lookup"><span data-stu-id="f6156-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


```powershell
PS C:\> # GitHub access token
PS C:\> $token = "68b08011223aac8bdd3388913a44rrsaa84fdf"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "GitHub1" `
                                           -RepoUrl "https://github.com/Contoso/TestSourceControl.git" `
                                           -SourceType "GitHub" `
                                           -Branch "master" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name    SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------ ---------- -------- -------------- -------
GitHub1 GitHub     master /Runbooks  True     True           https://github.com/Contoso/TestSourceControl...
```

## <span data-ttu-id="f6156-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6156-115">PARAMETERS</span></span>

### <span data-ttu-id="f6156-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="f6156-116">-AccessToken</span></span>
<span data-ttu-id="f6156-117">Token di accesso al controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="f6156-117">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6156-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f6156-118">-AutomationAccountName</span></span>
<span data-ttu-id="f6156-119">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="f6156-119">The automation account name.</span></span>

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

### <span data-ttu-id="f6156-120">-Branch</span><span class="sxs-lookup"><span data-stu-id="f6156-120">-Branch</span></span>
<span data-ttu-id="f6156-121">Ramo del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="f6156-121">The source control branch.</span></span>

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

### <span data-ttu-id="f6156-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6156-122">-DefaultProfile</span></span>
<span data-ttu-id="f6156-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6156-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6156-124">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6156-124">-Description</span></span>
<span data-ttu-id="f6156-125">Descrizione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="f6156-125">The source control description.</span></span>

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

### <span data-ttu-id="f6156-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="f6156-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="f6156-127">Proprietà publishRunbook del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="f6156-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="f6156-128">Se DoNotPublishRunbook è impostato, significa che manuali operativi utente verrà importato come "bozza".</span><span class="sxs-lookup"><span data-stu-id="f6156-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

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

### <span data-ttu-id="f6156-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="f6156-129">-EnableAutoSync</span></span>
<span data-ttu-id="f6156-130">Proprietà AutoSync per il controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="f6156-130">The autoSync property for the source control.</span></span>

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

### <span data-ttu-id="f6156-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="f6156-131">-FolderPath</span></span>
<span data-ttu-id="f6156-132">Percorso della cartella del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="f6156-132">The source control folder path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6156-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6156-133">-Name</span></span>
<span data-ttu-id="f6156-134">Nome del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="f6156-134">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6156-135">-Repourl</span><span class="sxs-lookup"><span data-stu-id="f6156-135">-RepoUrl</span></span>
<span data-ttu-id="f6156-136">URL del repository del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="f6156-136">The source control repo url.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6156-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6156-137">-ResourceGroupName</span></span>
<span data-ttu-id="f6156-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f6156-138">The resource group name.</span></span>

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

### <span data-ttu-id="f6156-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="f6156-139">-SourceType</span></span>
<span data-ttu-id="f6156-140">Tipo di controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="f6156-140">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6156-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f6156-141">-Confirm</span></span>
<span data-ttu-id="f6156-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6156-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6156-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6156-143">-WhatIf</span></span>
<span data-ttu-id="f6156-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6156-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6156-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f6156-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6156-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6156-146">CommonParameters</span></span>
<span data-ttu-id="f6156-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6156-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6156-148">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6156-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6156-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6156-149">INPUTS</span></span>

### <span data-ttu-id="f6156-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f6156-150">System.String</span></span>

## <span data-ttu-id="f6156-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6156-151">OUTPUTS</span></span>

### <span data-ttu-id="f6156-152">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="f6156-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="f6156-153">Note</span><span class="sxs-lookup"><span data-stu-id="f6156-153">NOTES</span></span>

## <span data-ttu-id="f6156-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6156-154">RELATED LINKS</span></span>
