---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
ms.openlocfilehash: 2ab7feb754bce7b160bf5aa47e225160649a70ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517131"
---
# <span data-ttu-id="bb7b9-101">Get-AzureRmAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="bb7b9-101">Get-AzureRmAutomationRegistrationInfo</span></span>

## <span data-ttu-id="bb7b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb7b9-102">SYNOPSIS</span></span>
<span data-ttu-id="bb7b9-103">Ottiene le informazioni di registrazione per l'onboarding di un nodo DSC o di un lavoratore ibrido all'automazione.</span><span class="sxs-lookup"><span data-stu-id="bb7b9-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb7b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb7b9-104">SYNTAX</span></span>

```
Get-AzureRmAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb7b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb7b9-105">DESCRIPTION</span></span>
<span data-ttu-id="bb7b9-106">Il cmdlet **Get-AzureRmAutomationRegistrationInfo** Ottiene l'endpoint e le chiavi necessarie per l'OnBoard di un nodo DSC (Desired state Configuration) o di un lavoratore ibrido in un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bb7b9-106">The **Get-AzureRmAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="bb7b9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb7b9-107">EXAMPLES</span></span>

### <span data-ttu-id="bb7b9-108">Esempio 1: ottenere le informazioni di registrazione</span><span class="sxs-lookup"><span data-stu-id="bb7b9-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzureRmAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="bb7b9-109">Questo comando consente di ottenere le informazioni di registrazione per l'account di automazione denominato AutomationAccount01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="bb7b9-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="bb7b9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb7b9-110">PARAMETERS</span></span>

### <span data-ttu-id="bb7b9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bb7b9-111">-AutomationAccountName</span></span>
<span data-ttu-id="bb7b9-112">Specifica il nome dell'account di automazione per cui questo cmdlet ottiene le informazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="bb7b9-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

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

### <span data-ttu-id="bb7b9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb7b9-113">-ResourceGroupName</span></span>
<span data-ttu-id="bb7b9-114">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bb7b9-114">Specifies the name of a resource group.</span></span>
<span data-ttu-id="bb7b9-115">Questo cmdlet ottiene le informazioni di registrazione per il gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bb7b9-115">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bb7b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb7b9-116">-DefaultProfile</span></span>
<span data-ttu-id="bb7b9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb7b9-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb7b9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb7b9-118">CommonParameters</span></span>
<span data-ttu-id="bb7b9-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb7b9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb7b9-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb7b9-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb7b9-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb7b9-121">INPUTS</span></span>

## <span data-ttu-id="bb7b9-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb7b9-122">OUTPUTS</span></span>

### <span data-ttu-id="bb7b9-123">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="bb7b9-123">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="bb7b9-124">Note</span><span class="sxs-lookup"><span data-stu-id="bb7b9-124">NOTES</span></span>

## <span data-ttu-id="bb7b9-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb7b9-125">RELATED LINKS</span></span>

[<span data-ttu-id="bb7b9-126">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="bb7b9-126">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="bb7b9-127">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="bb7b9-127">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="bb7b9-128">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="bb7b9-128">New-AzureRmAutomationKey</span></span>](./New-AzureRmAutomationKey.md)


