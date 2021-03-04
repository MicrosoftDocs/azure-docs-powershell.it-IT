---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: d9fbbed1beb67ce1bc8732cb5641c78705fd6a5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956494"
---
# <span data-ttu-id="94801-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="94801-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="94801-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94801-102">SYNOPSIS</span></span>
<span data-ttu-id="94801-103">Crea un controllo origine automazione.</span><span class="sxs-lookup"><span data-stu-id="94801-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="94801-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94801-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94801-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="94801-105">DESCRIPTION</span></span>
<span data-ttu-id="94801-106">Il cmdlet New-AzAutomationSourceControl crea una configurazione per collegare l'account di Automazione di Azure all'account TFVC di VSTS, a Git o a GitHub di VSTS.</span><span class="sxs-lookup"><span data-stu-id="94801-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="94801-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94801-107">EXAMPLES</span></span>

### <span data-ttu-id="94801-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="94801-108">Example 1</span></span>
<span data-ttu-id="94801-109">Creare una configurazione del controllo del codice sorgente per collegare l'account di Automazione di Azure al progetto TFVC di VSTS.</span><span class="sxs-lookup"><span data-stu-id="94801-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="94801-110">I progetti TFVC non hanno diramazioni, quindi il parametro Branch non è specificato.</span><span class="sxs-lookup"><span data-stu-id="94801-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://dev.azure.com/<accountname>/<adoprojectname>/_git/<repositoryname>" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://dev.azure.com/<accountname>/<adopro...
```

### <span data-ttu-id="94801-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="94801-111">Example 2</span></span>
<span data-ttu-id="94801-112">Creare una configurazione del controllo del codice sorgente per collegare l'account di Automazione di Azure al progetto Git di VSTS.</span><span class="sxs-lookup"><span data-stu-id="94801-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://dev.azure.com/<accountname>/<adoprojectname>/_git/<repositoryname>" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://dev.azure.com/<accountname>/<adopro...
```

### <span data-ttu-id="94801-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="94801-113">Example 3</span></span>
<span data-ttu-id="94801-114">Creare una configurazione del controllo del codice sorgente per collegare l'account di Automazione di Azure al progetto GitHub.</span><span class="sxs-lookup"><span data-stu-id="94801-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


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

## <span data-ttu-id="94801-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94801-115">PARAMETERS</span></span>

### <span data-ttu-id="94801-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="94801-116">-AccessToken</span></span>
<span data-ttu-id="94801-117">Token di accesso del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="94801-117">The source control access token.</span></span>

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

### <span data-ttu-id="94801-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="94801-118">-AutomationAccountName</span></span>
<span data-ttu-id="94801-119">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="94801-119">The automation account name.</span></span>

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

### <span data-ttu-id="94801-120">-Branch</span><span class="sxs-lookup"><span data-stu-id="94801-120">-Branch</span></span>
<span data-ttu-id="94801-121">Diramazione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="94801-121">The source control branch.</span></span>

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

### <span data-ttu-id="94801-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94801-122">-DefaultProfile</span></span>
<span data-ttu-id="94801-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94801-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94801-124">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="94801-124">-Description</span></span>
<span data-ttu-id="94801-125">Descrizione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="94801-125">The source control description.</span></span>

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

### <span data-ttu-id="94801-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="94801-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="94801-127">Proprietà publishRunbook del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="94801-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="94801-128">Se è impostato DoNotPublishRunbook, i runbook degli utenti verranno importati come "Bozza".</span><span class="sxs-lookup"><span data-stu-id="94801-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

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

### <span data-ttu-id="94801-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="94801-129">-EnableAutoSync</span></span>
<span data-ttu-id="94801-130">Proprietà autoSync per il controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="94801-130">The autoSync property for the source control.</span></span>

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

### <span data-ttu-id="94801-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="94801-131">-FolderPath</span></span>
<span data-ttu-id="94801-132">Percorso della cartella del controllo origine.</span><span class="sxs-lookup"><span data-stu-id="94801-132">The source control folder path.</span></span>

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

### <span data-ttu-id="94801-133">-Name</span><span class="sxs-lookup"><span data-stu-id="94801-133">-Name</span></span>
<span data-ttu-id="94801-134">Nome del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="94801-134">The source control name.</span></span>

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

### <span data-ttu-id="94801-135">-RepoUrl</span><span class="sxs-lookup"><span data-stu-id="94801-135">-RepoUrl</span></span>
<span data-ttu-id="94801-136">URL del repo del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="94801-136">The source control repo url.</span></span>

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

### <span data-ttu-id="94801-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94801-137">-ResourceGroupName</span></span>
<span data-ttu-id="94801-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="94801-138">The resource group name.</span></span>

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

### <span data-ttu-id="94801-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="94801-139">-SourceType</span></span>
<span data-ttu-id="94801-140">Tipo di controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="94801-140">The source control type.</span></span>

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

### <span data-ttu-id="94801-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94801-141">-Confirm</span></span>
<span data-ttu-id="94801-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94801-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94801-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94801-143">-WhatIf</span></span>
<span data-ttu-id="94801-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94801-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94801-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94801-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94801-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94801-146">CommonParameters</span></span>
<span data-ttu-id="94801-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94801-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94801-148">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94801-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94801-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="94801-149">INPUTS</span></span>

### <span data-ttu-id="94801-150">System.String</span><span class="sxs-lookup"><span data-stu-id="94801-150">System.String</span></span>

## <span data-ttu-id="94801-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94801-151">OUTPUTS</span></span>

### <span data-ttu-id="94801-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="94801-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="94801-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="94801-153">NOTES</span></span>

## <span data-ttu-id="94801-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94801-154">RELATED LINKS</span></span>
