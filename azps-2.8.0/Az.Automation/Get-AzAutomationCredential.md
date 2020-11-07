---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3a13605618c5cda3c247cd6b0812732ce018bafe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675823"
---
# <span data-ttu-id="adc58-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="adc58-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="adc58-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="adc58-102">SYNOPSIS</span></span>
<span data-ttu-id="adc58-103">Ottiene le credenziali di automazione.</span><span class="sxs-lookup"><span data-stu-id="adc58-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="adc58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="adc58-104">SYNTAX</span></span>

### <span data-ttu-id="adc58-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="adc58-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adc58-106">ByName</span><span class="sxs-lookup"><span data-stu-id="adc58-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adc58-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adc58-107">DESCRIPTION</span></span>
<span data-ttu-id="adc58-108">Il cmdlet **Get-AzAutomationCredential** ottiene una o più credenziali di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="adc58-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="adc58-109">Per impostazione predefinita, vengono restituite tutte le credenziali.</span><span class="sxs-lookup"><span data-stu-id="adc58-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="adc58-110">Specificare il nome di una credenziale per ottenere una specifica credenziale.</span><span class="sxs-lookup"><span data-stu-id="adc58-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="adc58-111">Per motivi di sicurezza, questo cmdlet non restituisce le password delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="adc58-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="adc58-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="adc58-112">EXAMPLES</span></span>

### <span data-ttu-id="adc58-113">Esempio 1: ottenere tutte le credenziali</span><span class="sxs-lookup"><span data-stu-id="adc58-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="adc58-114">Questo comando consente di ottenere metadati per tutte le credenziali nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="adc58-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="adc58-115">Esempio 2: ottenere una credenziale</span><span class="sxs-lookup"><span data-stu-id="adc58-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="adc58-116">Questo comando consente di ottenere metadati per le credenziali denominate ContosoCredential nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="adc58-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="adc58-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="adc58-117">PARAMETERS</span></span>

### <span data-ttu-id="adc58-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="adc58-118">-AutomationAccountName</span></span>
<span data-ttu-id="adc58-119">Specifica il nome dell'account di automazione per cui questo cmdlet recupera le credenziali.</span><span class="sxs-lookup"><span data-stu-id="adc58-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="adc58-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc58-120">-DefaultProfile</span></span>
<span data-ttu-id="adc58-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="adc58-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adc58-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="adc58-122">-Name</span></span>
<span data-ttu-id="adc58-123">Specifica il nome di una credenziale da recuperare.</span><span class="sxs-lookup"><span data-stu-id="adc58-123">Specifies the name of a credential to retrieve.</span></span>

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

### <span data-ttu-id="adc58-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adc58-124">-ResourceGroupName</span></span>
<span data-ttu-id="adc58-125">Specifica il gruppo di risorse per cui questo cmdlet recupera le credenziali.</span><span class="sxs-lookup"><span data-stu-id="adc58-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="adc58-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc58-126">CommonParameters</span></span>
<span data-ttu-id="adc58-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adc58-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc58-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adc58-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc58-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="adc58-129">INPUTS</span></span>

### <span data-ttu-id="adc58-130">System. String</span><span class="sxs-lookup"><span data-stu-id="adc58-130">System.String</span></span>

## <span data-ttu-id="adc58-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="adc58-131">OUTPUTS</span></span>

### <span data-ttu-id="adc58-132">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="adc58-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="adc58-133">Note</span><span class="sxs-lookup"><span data-stu-id="adc58-133">NOTES</span></span>

## <span data-ttu-id="adc58-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="adc58-134">RELATED LINKS</span></span>

[<span data-ttu-id="adc58-135">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="adc58-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="adc58-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="adc58-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="adc58-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="adc58-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


