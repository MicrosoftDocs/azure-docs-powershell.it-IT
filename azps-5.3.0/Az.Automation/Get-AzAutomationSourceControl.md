---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 42472efdde4ccf96f12a0617d9a86175eed13d1c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478667"
---
# <span data-ttu-id="4b098-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="4b098-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="4b098-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b098-102">SYNOPSIS</span></span>
<span data-ttu-id="4b098-103">Ottiene un elenco dei controlli di origine di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4b098-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="4b098-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b098-104">SYNTAX</span></span>

### <span data-ttu-id="4b098-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4b098-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b098-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4b098-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b098-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b098-107">DESCRIPTION</span></span>
<span data-ttu-id="4b098-108">Il cmdlet Get-AzAutomationSourceControl ottiene i controlli di origine di automazione.</span><span class="sxs-lookup"><span data-stu-id="4b098-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="4b098-109">Per ottenere uno specifico controllo del codice sorgente, specificarne il nome.</span><span class="sxs-lookup"><span data-stu-id="4b098-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="4b098-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b098-110">EXAMPLES</span></span>

### <span data-ttu-id="4b098-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4b098-111">Example 1</span></span>
<span data-ttu-id="4b098-112">Questo comando ottiene un controllo origine di automazione denominato VSTSNative nell'account denominato devAccount.</span><span class="sxs-lookup"><span data-stu-id="4b098-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="4b098-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b098-113">PARAMETERS</span></span>

### <span data-ttu-id="4b098-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4b098-114">-AutomationAccountName</span></span>
<span data-ttu-id="4b098-115">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="4b098-115">The automation account name.</span></span>

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

### <span data-ttu-id="4b098-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b098-116">-DefaultProfile</span></span>
<span data-ttu-id="4b098-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b098-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b098-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b098-118">-Name</span></span>
<span data-ttu-id="4b098-119">Nome del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="4b098-119">The source control name.</span></span>

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

### <span data-ttu-id="4b098-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b098-120">-ResourceGroupName</span></span>
<span data-ttu-id="4b098-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b098-121">The resource group name.</span></span>

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

### <span data-ttu-id="4b098-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="4b098-122">-SourceType</span></span>
<span data-ttu-id="4b098-123">Tipo di controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="4b098-123">The source control type.</span></span>

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

### <span data-ttu-id="4b098-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b098-124">CommonParameters</span></span>
<span data-ttu-id="4b098-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b098-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b098-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b098-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b098-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b098-127">INPUTS</span></span>

### <span data-ttu-id="4b098-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4b098-128">System.String</span></span>

## <span data-ttu-id="4b098-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b098-129">OUTPUTS</span></span>

### <span data-ttu-id="4b098-130">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="4b098-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="4b098-131">Note</span><span class="sxs-lookup"><span data-stu-id="4b098-131">NOTES</span></span>

## <span data-ttu-id="4b098-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b098-132">RELATED LINKS</span></span>
