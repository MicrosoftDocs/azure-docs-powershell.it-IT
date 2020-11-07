---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 70b92cd7762b42fba7ae890cd22b529ba80318ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675831"
---
# <span data-ttu-id="a2dde-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a2dde-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="a2dde-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2dde-102">SYNOPSIS</span></span>
<span data-ttu-id="a2dde-103">Ottiene i certificati di automazione.</span><span class="sxs-lookup"><span data-stu-id="a2dde-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="a2dde-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2dde-104">SYNTAX</span></span>

### <span data-ttu-id="a2dde-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a2dde-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2dde-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="a2dde-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2dde-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2dde-107">DESCRIPTION</span></span>
<span data-ttu-id="a2dde-108">Il cmdlet **Get-AzAutomationCertificate** ottiene uno o più certificati di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="a2dde-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="a2dde-109">Per impostazione predefinita, questo cmdlet ottiene tutti i certificati.</span><span class="sxs-lookup"><span data-stu-id="a2dde-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="a2dde-110">Specificare il nome di un certificato per ottenere un certificato specifico.</span><span class="sxs-lookup"><span data-stu-id="a2dde-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="a2dde-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2dde-111">EXAMPLES</span></span>

### <span data-ttu-id="a2dde-112">Esempio 1: ottenere tutti i certificati</span><span class="sxs-lookup"><span data-stu-id="a2dde-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="a2dde-113">Questo comando consente di ottenere metadati per tutti i certificati nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a2dde-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="a2dde-114">Esempio 2: ottenere un certificato</span><span class="sxs-lookup"><span data-stu-id="a2dde-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="a2dde-115">Questo comando consente di ottenere metadati per il certificato denominato ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="a2dde-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="a2dde-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2dde-116">PARAMETERS</span></span>

### <span data-ttu-id="a2dde-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a2dde-117">-AutomationAccountName</span></span>
<span data-ttu-id="a2dde-118">Specifica il nome dell'account di automazione per cui questo cmdlet recupera un certificato.</span><span class="sxs-lookup"><span data-stu-id="a2dde-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="a2dde-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2dde-119">-DefaultProfile</span></span>
<span data-ttu-id="a2dde-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a2dde-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2dde-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="a2dde-121">-Name</span></span>
<span data-ttu-id="a2dde-122">Specifica il nome di un certificato da recuperare.</span><span class="sxs-lookup"><span data-stu-id="a2dde-122">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2dde-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2dde-123">-ResourceGroupName</span></span>
<span data-ttu-id="a2dde-124">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="a2dde-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="a2dde-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2dde-125">CommonParameters</span></span>
<span data-ttu-id="a2dde-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2dde-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2dde-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2dde-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2dde-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2dde-128">INPUTS</span></span>

### <span data-ttu-id="a2dde-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a2dde-129">System.String</span></span>

## <span data-ttu-id="a2dde-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2dde-130">OUTPUTS</span></span>

### <span data-ttu-id="a2dde-131">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="a2dde-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="a2dde-132">Note</span><span class="sxs-lookup"><span data-stu-id="a2dde-132">NOTES</span></span>

## <span data-ttu-id="a2dde-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2dde-133">RELATED LINKS</span></span>

[<span data-ttu-id="a2dde-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a2dde-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="a2dde-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a2dde-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="a2dde-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="a2dde-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)

