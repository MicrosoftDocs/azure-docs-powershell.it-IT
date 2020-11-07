---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
ms.openlocfilehash: c92e42f49368e894006da0f7afeb9ffcf7e4a564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520302"
---
# <span data-ttu-id="0161c-101">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="0161c-101">Get-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="0161c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0161c-102">SYNOPSIS</span></span>
<span data-ttu-id="0161c-103">Ottiene le credenziali di automazione.</span><span class="sxs-lookup"><span data-stu-id="0161c-103">Gets Automation credentials.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0161c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0161c-104">SYNTAX</span></span>

### <span data-ttu-id="0161c-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0161c-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0161c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0161c-106">ByName</span></span>
```
Get-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0161c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0161c-107">DESCRIPTION</span></span>
<span data-ttu-id="0161c-108">Il cmdlet **Get-AzureRmAutomationCredential** ottiene una o più credenziali di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="0161c-108">The **Get-AzureRmAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="0161c-109">Per impostazione predefinita, vengono restituite tutte le credenziali.</span><span class="sxs-lookup"><span data-stu-id="0161c-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="0161c-110">Specificare il nome di una credenziale per ottenere una specifica credenziale.</span><span class="sxs-lookup"><span data-stu-id="0161c-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="0161c-111">Per motivi di sicurezza, questo cmdlet non restituisce le password delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="0161c-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="0161c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0161c-112">EXAMPLES</span></span>

### <span data-ttu-id="0161c-113">Esempio 1: ottenere tutte le credenziali</span><span class="sxs-lookup"><span data-stu-id="0161c-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="0161c-114">Questo comando consente di ottenere metadati per tutte le credenziali nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0161c-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="0161c-115">Esempio 2: ottenere una credenziale</span><span class="sxs-lookup"><span data-stu-id="0161c-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="0161c-116">Questo comando consente di ottenere metadati per le credenziali denominate ContosoCredential nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0161c-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0161c-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0161c-117">PARAMETERS</span></span>

### <span data-ttu-id="0161c-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0161c-118">-AutomationAccountName</span></span>
<span data-ttu-id="0161c-119">Specifica il nome dell'account di automazione per cui questo cmdlet recupera le credenziali.</span><span class="sxs-lookup"><span data-stu-id="0161c-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="0161c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0161c-120">-DefaultProfile</span></span>
<span data-ttu-id="0161c-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0161c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0161c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0161c-122">-Name</span></span>
<span data-ttu-id="0161c-123">Specifica il nome di una credenziale da recuperare.</span><span class="sxs-lookup"><span data-stu-id="0161c-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0161c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0161c-124">-ResourceGroupName</span></span>
<span data-ttu-id="0161c-125">Specifica il gruppo di risorse per cui questo cmdlet recupera le credenziali.</span><span class="sxs-lookup"><span data-stu-id="0161c-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="0161c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0161c-126">CommonParameters</span></span>
<span data-ttu-id="0161c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0161c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0161c-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0161c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0161c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0161c-129">INPUTS</span></span>

### <span data-ttu-id="0161c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0161c-130">System.String</span></span>

## <span data-ttu-id="0161c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0161c-131">OUTPUTS</span></span>

### <span data-ttu-id="0161c-132">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="0161c-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="0161c-133">Note</span><span class="sxs-lookup"><span data-stu-id="0161c-133">NOTES</span></span>

## <span data-ttu-id="0161c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0161c-134">RELATED LINKS</span></span>

[<span data-ttu-id="0161c-135">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="0161c-135">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="0161c-136">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="0161c-136">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="0161c-137">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="0161c-137">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)

