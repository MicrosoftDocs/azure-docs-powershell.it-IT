---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: 226791db9057fe0f8aa246fab546dd4af7303529
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031417"
---
# <span data-ttu-id="bc609-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="bc609-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="bc609-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bc609-102">SYNOPSIS</span></span>
<span data-ttu-id="bc609-103">Ottiene le informazioni di registrazione per l'onboarding di un nodo DSC o di un lavoratore ibrido all'automazione.</span><span class="sxs-lookup"><span data-stu-id="bc609-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="bc609-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bc609-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc609-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc609-105">DESCRIPTION</span></span>
<span data-ttu-id="bc609-106">Il cmdlet **Get-AzAutomationRegistrationInfo** Ottiene l'endpoint e le chiavi necessarie per l'OnBoard di un nodo DSC (Desired state Configuration) o di un lavoratore ibrido in un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bc609-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="bc609-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bc609-107">EXAMPLES</span></span>

### <span data-ttu-id="bc609-108">Esempio 1: ottenere le informazioni di registrazione</span><span class="sxs-lookup"><span data-stu-id="bc609-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="bc609-109">Questo comando consente di ottenere le informazioni di registrazione per l'account di automazione denominato AutomationAccount01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="bc609-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="bc609-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bc609-110">PARAMETERS</span></span>

### <span data-ttu-id="bc609-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bc609-111">-AutomationAccountName</span></span>
<span data-ttu-id="bc609-112">Specifica il nome dell'account di automazione per cui questo cmdlet ottiene le informazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="bc609-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="bc609-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc609-113">-DefaultProfile</span></span>
<span data-ttu-id="bc609-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bc609-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc609-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc609-115">-ResourceGroupName</span></span>
<span data-ttu-id="bc609-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bc609-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="bc609-117">Questo cmdlet ottiene le informazioni di registrazione per il gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bc609-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bc609-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc609-118">CommonParameters</span></span>
<span data-ttu-id="bc609-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc609-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc609-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc609-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc609-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bc609-121">INPUTS</span></span>

### <span data-ttu-id="bc609-122">System. String</span><span class="sxs-lookup"><span data-stu-id="bc609-122">System.String</span></span>

## <span data-ttu-id="bc609-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bc609-123">OUTPUTS</span></span>

### <span data-ttu-id="bc609-124">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="bc609-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="bc609-125">Note</span><span class="sxs-lookup"><span data-stu-id="bc609-125">NOTES</span></span>

## <span data-ttu-id="bc609-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bc609-126">RELATED LINKS</span></span>

[<span data-ttu-id="bc609-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="bc609-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="bc609-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="bc609-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="bc609-129">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="bc609-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


