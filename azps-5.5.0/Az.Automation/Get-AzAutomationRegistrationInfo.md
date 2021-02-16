---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: 226791db9057fe0f8aa246fab546dd4af7303529
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199662"
---
# <span data-ttu-id="16e4a-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="16e4a-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="16e4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="16e4a-103">Recupera le informazioni di registrazione per l'onboarding di un nodo DSC o di un utente ibrido all'automazione.</span><span class="sxs-lookup"><span data-stu-id="16e4a-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="16e4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16e4a-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16e4a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="16e4a-105">DESCRIPTION</span></span>
<span data-ttu-id="16e4a-106">Il cmdlet **Get-AzAutomationRegistrationInfo** recupera gli endpoint e le chiavi necessari per aggiungere un nodo DSC (Desired State Configuration) o un utente ibrido in un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="16e4a-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="16e4a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16e4a-107">EXAMPLES</span></span>

### <span data-ttu-id="16e4a-108">Esempio 1: Ottenere le informazioni di registrazione</span><span class="sxs-lookup"><span data-stu-id="16e4a-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="16e4a-109">Questo comando recupera le informazioni di registrazione per l'account di automazione denominato AutomationAccount01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="16e4a-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="16e4a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16e4a-110">PARAMETERS</span></span>

### <span data-ttu-id="16e4a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="16e4a-111">-AutomationAccountName</span></span>
<span data-ttu-id="16e4a-112">Specifica il nome dell'account di automazione per cui questo cmdlet ottiene le informazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="16e4a-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="16e4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e4a-113">-DefaultProfile</span></span>
<span data-ttu-id="16e4a-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="16e4a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16e4a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16e4a-115">-ResourceGroupName</span></span>
<span data-ttu-id="16e4a-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="16e4a-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="16e4a-117">Questo cmdlet ottiene le informazioni di registrazione per il gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="16e4a-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="16e4a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e4a-118">CommonParameters</span></span>
<span data-ttu-id="16e4a-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e4a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e4a-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16e4a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e4a-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="16e4a-121">INPUTS</span></span>

### <span data-ttu-id="16e4a-122">System.String</span><span class="sxs-lookup"><span data-stu-id="16e4a-122">System.String</span></span>

## <span data-ttu-id="16e4a-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16e4a-123">OUTPUTS</span></span>

### <span data-ttu-id="16e4a-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="16e4a-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="16e4a-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="16e4a-125">NOTES</span></span>

## <span data-ttu-id="16e4a-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16e4a-126">RELATED LINKS</span></span>

[<span data-ttu-id="16e4a-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="16e4a-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="16e4a-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="16e4a-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="16e4a-129">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="16e4a-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


