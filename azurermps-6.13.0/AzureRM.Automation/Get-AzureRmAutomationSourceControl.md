---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControl.md
ms.openlocfilehash: 3e7affd09e8c24c1d3c1759e78ea09a0c849ff32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519770"
---
# <span data-ttu-id="375ab-101">Get-AzureRmAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="375ab-101">Get-AzureRmAutomationSourceControl</span></span>

## <span data-ttu-id="375ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="375ab-102">SYNOPSIS</span></span>
<span data-ttu-id="375ab-103">Ottiene un elenco dei controlli di origine di Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="375ab-103">Gets a list of Azure Automation source controls.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="375ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="375ab-104">SYNTAX</span></span>

### <span data-ttu-id="375ab-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="375ab-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="375ab-106">ByName</span><span class="sxs-lookup"><span data-stu-id="375ab-106">ByName</span></span>
```
Get-AzureRmAutomationSourceControl -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="375ab-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="375ab-107">DESCRIPTION</span></span>
<span data-ttu-id="375ab-108">Il cmdlet Get-AzureRmAutomationSourceControl ottiene i controlli di origine di automazione.</span><span class="sxs-lookup"><span data-stu-id="375ab-108">The Get-AzureRmAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="375ab-109">Per ottenere uno specifico controllo del codice sorgente, specificarne il nome.</span><span class="sxs-lookup"><span data-stu-id="375ab-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="375ab-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="375ab-110">EXAMPLES</span></span>

### <span data-ttu-id="375ab-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="375ab-111">Example 1</span></span>
<span data-ttu-id="375ab-112">Questo comando ottiene un controllo origine di automazione denominato VSTSNative nell'account denominato devAccount.</span><span class="sxs-lookup"><span data-stu-id="375ab-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="375ab-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="375ab-113">PARAMETERS</span></span>

### <span data-ttu-id="375ab-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="375ab-114">-AutomationAccountName</span></span>
<span data-ttu-id="375ab-115">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="375ab-115">The automation account name.</span></span>

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

### <span data-ttu-id="375ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="375ab-116">-DefaultProfile</span></span>
<span data-ttu-id="375ab-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="375ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="375ab-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="375ab-118">-Name</span></span>
<span data-ttu-id="375ab-119">Nome del controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="375ab-119">The source control name.</span></span>

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

### <span data-ttu-id="375ab-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="375ab-120">-ResourceGroupName</span></span>
<span data-ttu-id="375ab-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="375ab-121">The resource group name.</span></span>

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

### <span data-ttu-id="375ab-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="375ab-122">-SourceType</span></span>
<span data-ttu-id="375ab-123">Tipo di controllo del codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="375ab-123">The source control type.</span></span>

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

### <span data-ttu-id="375ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="375ab-124">CommonParameters</span></span>
<span data-ttu-id="375ab-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="375ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="375ab-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="375ab-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="375ab-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="375ab-127">INPUTS</span></span>

### <span data-ttu-id="375ab-128">System. String</span><span class="sxs-lookup"><span data-stu-id="375ab-128">System.String</span></span>

## <span data-ttu-id="375ab-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="375ab-129">OUTPUTS</span></span>

### <span data-ttu-id="375ab-130">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="375ab-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="375ab-131">Note</span><span class="sxs-lookup"><span data-stu-id="375ab-131">NOTES</span></span>

## <span data-ttu-id="375ab-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="375ab-132">RELATED LINKS</span></span>
