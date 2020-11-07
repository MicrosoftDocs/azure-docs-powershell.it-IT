---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/update-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
ms.openlocfilehash: ee3b7b7cdbe098c6892782ca4084bd2fb7e6a615
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864841"
---
# <span data-ttu-id="49ecb-101">Update-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="49ecb-101">Update-AzAutomationSourceControl</span></span>

## <span data-ttu-id="49ecb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="49ecb-103">Aggiorna un controllo del codice sorgente di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="49ecb-103">Updates an Azure Automation source control.</span></span>

## <span data-ttu-id="49ecb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49ecb-104">SYNTAX</span></span>

```
Update-AzAutomationSourceControl -Name <String> [-AccessToken <SecureString>] [-FolderPath <String>]
 [-Branch <String>] [-Description <String>] [-AutoSync <Boolean>] [-PublishRunbook <Boolean>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49ecb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49ecb-105">DESCRIPTION</span></span>
<span data-ttu-id="49ecb-106">Il cmdlet Update-AzAutomationSourceControl modifica il valore di un campo in un controllo del codice sorgente in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="49ecb-106">The Update-AzAutomationSourceControl cmdlet modifies the value of a field in a source control in Azure Automation.</span></span>

## <span data-ttu-id="49ecb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49ecb-107">EXAMPLES</span></span>

### <span data-ttu-id="49ecb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="49ecb-108">Example 1</span></span>
<span data-ttu-id="49ecb-109">Questo comando imposta il campo PublishRunbook su false per il controllo del codice sorgente di Azure Automation denominato VSTSNative nell'account denominato devAccount.</span><span class="sxs-lookup"><span data-stu-id="49ecb-109">This commands sets the PublishRunbook field to false for the Azure Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
Update-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                      -AutomationAccountName "devAccount" `
                                      -Name "VSTSNative" `
                                      -PublishRunbook $false 

Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    False          https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="49ecb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49ecb-110">PARAMETERS</span></span>

### <span data-ttu-id="49ecb-111">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="49ecb-111">-AccessToken</span></span>
<span data-ttu-id="49ecb-112">Token di accesso al controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="49ecb-112">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ecb-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="49ecb-113">-AutomationAccountName</span></span>
<span data-ttu-id="49ecb-114">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="49ecb-114">The automation account name.</span></span>

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

### <span data-ttu-id="49ecb-115">-Sincronizzazione automatica</span><span class="sxs-lookup"><span data-stu-id="49ecb-115">-AutoSync</span></span>
<span data-ttu-id="49ecb-116">Proprietà AutoSync per il controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="49ecb-116">The autoSync property for the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ecb-117">-Branch</span><span class="sxs-lookup"><span data-stu-id="49ecb-117">-Branch</span></span>
<span data-ttu-id="49ecb-118">Ramo del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="49ecb-118">The source control branch.</span></span>

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

### <span data-ttu-id="49ecb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49ecb-119">-DefaultProfile</span></span>
<span data-ttu-id="49ecb-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49ecb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49ecb-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="49ecb-121">-Description</span></span>
<span data-ttu-id="49ecb-122">Descrizione del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="49ecb-122">The source control description.</span></span>

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

### <span data-ttu-id="49ecb-123">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="49ecb-123">-FolderPath</span></span>
<span data-ttu-id="49ecb-124">Percorso della cartella del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="49ecb-124">The source control folder path.</span></span>

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

### <span data-ttu-id="49ecb-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="49ecb-125">-Name</span></span>
<span data-ttu-id="49ecb-126">Nome del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="49ecb-126">The source control name.</span></span>

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

### <span data-ttu-id="49ecb-127">-PublishRunbook</span><span class="sxs-lookup"><span data-stu-id="49ecb-127">-PublishRunbook</span></span>
<span data-ttu-id="49ecb-128">Proprietà publishRunbook del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="49ecb-128">The publishRunbook property of the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ecb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49ecb-129">-ResourceGroupName</span></span>
<span data-ttu-id="49ecb-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="49ecb-130">The resource group name.</span></span>

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

### <span data-ttu-id="49ecb-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="49ecb-131">-Confirm</span></span>
<span data-ttu-id="49ecb-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49ecb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49ecb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49ecb-133">-WhatIf</span></span>
<span data-ttu-id="49ecb-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49ecb-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49ecb-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49ecb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49ecb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ecb-136">CommonParameters</span></span>
<span data-ttu-id="49ecb-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49ecb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ecb-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ecb-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ecb-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49ecb-139">INPUTS</span></span>

### <span data-ttu-id="49ecb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="49ecb-140">System.String</span></span>

## <span data-ttu-id="49ecb-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49ecb-141">OUTPUTS</span></span>

### <span data-ttu-id="49ecb-142">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="49ecb-142">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="49ecb-143">Note</span><span class="sxs-lookup"><span data-stu-id="49ecb-143">NOTES</span></span>

## <span data-ttu-id="49ecb-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49ecb-144">RELATED LINKS</span></span>
