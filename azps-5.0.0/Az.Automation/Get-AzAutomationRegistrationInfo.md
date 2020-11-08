---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRegistrationInfo.md
ms.openlocfilehash: 226791db9057fe0f8aa246fab546dd4af7303529
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201598"
---
# <span data-ttu-id="574fd-101">Get-AzAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="574fd-101">Get-AzAutomationRegistrationInfo</span></span>

## <span data-ttu-id="574fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="574fd-102">SYNOPSIS</span></span>
<span data-ttu-id="574fd-103">Ottiene le informazioni di registrazione per l'onboarding di un nodo DSC o di un lavoratore ibrido all'automazione.</span><span class="sxs-lookup"><span data-stu-id="574fd-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

## <span data-ttu-id="574fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="574fd-104">SYNTAX</span></span>

```
Get-AzAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="574fd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="574fd-105">DESCRIPTION</span></span>
<span data-ttu-id="574fd-106">Il cmdlet **Get-AzAutomationRegistrationInfo** Ottiene l'endpoint e le chiavi necessarie per l'OnBoard di un nodo DSC (Desired state Configuration) o di un lavoratore ibrido in un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="574fd-106">The **Get-AzAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="574fd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="574fd-107">EXAMPLES</span></span>

### <span data-ttu-id="574fd-108">Esempio 1: ottenere le informazioni di registrazione</span><span class="sxs-lookup"><span data-stu-id="574fd-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="574fd-109">Questo comando consente di ottenere le informazioni di registrazione per l'account di automazione denominato AutomationAccount01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="574fd-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="574fd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="574fd-110">PARAMETERS</span></span>

### <span data-ttu-id="574fd-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="574fd-111">-AutomationAccountName</span></span>
<span data-ttu-id="574fd-112">Specifica il nome dell'account di automazione per cui questo cmdlet ottiene le informazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="574fd-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="574fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="574fd-113">-DefaultProfile</span></span>
<span data-ttu-id="574fd-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="574fd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="574fd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="574fd-115">-ResourceGroupName</span></span>
<span data-ttu-id="574fd-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="574fd-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="574fd-117">Questo cmdlet ottiene le informazioni di registrazione per il gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="574fd-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="574fd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="574fd-118">CommonParameters</span></span>
<span data-ttu-id="574fd-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="574fd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="574fd-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="574fd-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="574fd-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="574fd-121">INPUTS</span></span>

### <span data-ttu-id="574fd-122">System. String</span><span class="sxs-lookup"><span data-stu-id="574fd-122">System.String</span></span>

## <span data-ttu-id="574fd-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="574fd-123">OUTPUTS</span></span>

### <span data-ttu-id="574fd-124">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="574fd-124">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="574fd-125">Note</span><span class="sxs-lookup"><span data-stu-id="574fd-125">NOTES</span></span>

## <span data-ttu-id="574fd-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="574fd-126">RELATED LINKS</span></span>

[<span data-ttu-id="574fd-127">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="574fd-127">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="574fd-128">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="574fd-128">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="574fd-129">New-AzAutomationKey</span><span class="sxs-lookup"><span data-stu-id="574fd-129">New-AzAutomationKey</span></span>](./New-AzAutomationKey.md)


