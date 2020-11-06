---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 09823BE3-A98B-42EF-B6F4-99F95F2B342E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationregistrationinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationRegistrationInfo.md
ms.openlocfilehash: dfdd4d4de935d83beaa20246c490ded7b23dcc9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508411"
---
# <span data-ttu-id="478f2-101">Get-AzureRmAutomationRegistrationInfo</span><span class="sxs-lookup"><span data-stu-id="478f2-101">Get-AzureRmAutomationRegistrationInfo</span></span>

## <span data-ttu-id="478f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="478f2-102">SYNOPSIS</span></span>
<span data-ttu-id="478f2-103">Ottiene le informazioni di registrazione per l'onboarding di un nodo DSC o di un lavoratore ibrido all'automazione.</span><span class="sxs-lookup"><span data-stu-id="478f2-103">Gets registration information for onboarding a DSC node or hybrid worker to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="478f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="478f2-104">SYNTAX</span></span>

```
Get-AzureRmAutomationRegistrationInfo [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="478f2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="478f2-105">DESCRIPTION</span></span>
<span data-ttu-id="478f2-106">Il cmdlet **Get-AzureRmAutomationRegistrationInfo** Ottiene l'endpoint e le chiavi necessarie per l'OnBoard di un nodo DSC (Desired state Configuration) o di un lavoratore ibrido in un account di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="478f2-106">The **Get-AzureRmAutomationRegistrationInfo** cmdlet gets the endpoint and keys required to onboard a Desired State Configuration (DSC) node or hybrid worker into an Azure Automation account.</span></span>

## <span data-ttu-id="478f2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="478f2-107">EXAMPLES</span></span>

### <span data-ttu-id="478f2-108">Esempio 1: ottenere le informazioni di registrazione</span><span class="sxs-lookup"><span data-stu-id="478f2-108">Example 1: Get registration information</span></span>
```
PS C:\>Get-AzureRmAutomationRegistrationInfo -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="478f2-109">Questo comando consente di ottenere le informazioni di registrazione per l'account di automazione denominato AutomationAccount01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="478f2-109">This command gets the registration information for the Automation account named AutomationAccount01 in the Resource Group named ResourceGroup01.</span></span>

## <span data-ttu-id="478f2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="478f2-110">PARAMETERS</span></span>

### <span data-ttu-id="478f2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="478f2-111">-AutomationAccountName</span></span>
<span data-ttu-id="478f2-112">Specifica il nome dell'account di automazione per cui questo cmdlet ottiene le informazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="478f2-112">Specifies the name of Automation account for which this cmdlet gets registration information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="478f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="478f2-113">-DefaultProfile</span></span>
<span data-ttu-id="478f2-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="478f2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="478f2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="478f2-115">-ResourceGroupName</span></span>
<span data-ttu-id="478f2-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="478f2-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="478f2-117">Questo cmdlet ottiene le informazioni di registrazione per il gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="478f2-117">This cmdlet gets registration information for the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="478f2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="478f2-118">CommonParameters</span></span>
<span data-ttu-id="478f2-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="478f2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="478f2-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="478f2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="478f2-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="478f2-121">INPUTS</span></span>

### <span data-ttu-id="478f2-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="478f2-122">None</span></span>
<span data-ttu-id="478f2-123">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="478f2-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="478f2-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="478f2-124">OUTPUTS</span></span>

### <span data-ttu-id="478f2-125">Microsoft. Azure. Commands. Automation. Model. AgentRegistration</span><span class="sxs-lookup"><span data-stu-id="478f2-125">Microsoft.Azure.Commands.Automation.Model.AgentRegistration</span></span>

## <span data-ttu-id="478f2-126">Note</span><span class="sxs-lookup"><span data-stu-id="478f2-126">NOTES</span></span>

## <span data-ttu-id="478f2-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="478f2-127">RELATED LINKS</span></span>

[<span data-ttu-id="478f2-128">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="478f2-128">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="478f2-129">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="478f2-129">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="478f2-130">New-AzureRmAutomationKey</span><span class="sxs-lookup"><span data-stu-id="478f2-130">New-AzureRmAutomationKey</span></span>](./New-AzureRmAutomationKey.md)


