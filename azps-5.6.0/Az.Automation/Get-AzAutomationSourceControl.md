---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 051eee1c191662e6ca4eb56e34088af651ea69f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014158"
---
# <span data-ttu-id="41bc5-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="41bc5-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="41bc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="41bc5-103">Ottiene un elenco di controlli origine di Automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="41bc5-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="41bc5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41bc5-104">SYNTAX</span></span>

### <span data-ttu-id="41bc5-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41bc5-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41bc5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="41bc5-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41bc5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="41bc5-107">DESCRIPTION</span></span>
<span data-ttu-id="41bc5-108">Il cmdlet Get-AzAutomationSourceControl ottiene i controlli origine di automazione.</span><span class="sxs-lookup"><span data-stu-id="41bc5-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="41bc5-109">Per ottenere un controllo del codice sorgente specifico, specificarne il nome.</span><span class="sxs-lookup"><span data-stu-id="41bc5-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="41bc5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41bc5-110">EXAMPLES</span></span>

### <span data-ttu-id="41bc5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="41bc5-111">Example 1</span></span>
<span data-ttu-id="41bc5-112">Questo comando recupera un controllo origine di automazione denominato VSTSNative nell'account denominato devAccount.</span><span class="sxs-lookup"><span data-stu-id="41bc5-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="41bc5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41bc5-113">PARAMETERS</span></span>

### <span data-ttu-id="41bc5-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="41bc5-114">-AutomationAccountName</span></span>
<span data-ttu-id="41bc5-115">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="41bc5-115">The automation account name.</span></span>

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

### <span data-ttu-id="41bc5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41bc5-116">-DefaultProfile</span></span>
<span data-ttu-id="41bc5-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41bc5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41bc5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="41bc5-118">-Name</span></span>
<span data-ttu-id="41bc5-119">Nome del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="41bc5-119">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41bc5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41bc5-120">-ResourceGroupName</span></span>
<span data-ttu-id="41bc5-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="41bc5-121">The resource group name.</span></span>

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

### <span data-ttu-id="41bc5-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="41bc5-122">-SourceType</span></span>
<span data-ttu-id="41bc5-123">Tipo di controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="41bc5-123">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41bc5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41bc5-124">CommonParameters</span></span>
<span data-ttu-id="41bc5-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41bc5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41bc5-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41bc5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41bc5-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="41bc5-127">INPUTS</span></span>

### <span data-ttu-id="41bc5-128">System.String</span><span class="sxs-lookup"><span data-stu-id="41bc5-128">System.String</span></span>

## <span data-ttu-id="41bc5-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41bc5-129">OUTPUTS</span></span>

### <span data-ttu-id="41bc5-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="41bc5-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="41bc5-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="41bc5-131">NOTES</span></span>

## <span data-ttu-id="41bc5-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41bc5-132">RELATED LINKS</span></span>
