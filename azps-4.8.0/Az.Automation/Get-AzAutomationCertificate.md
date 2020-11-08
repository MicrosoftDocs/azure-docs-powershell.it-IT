---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 3a504ba081852ff3bb84a6ace432b394a2b2b478
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032683"
---
# <span data-ttu-id="2fce2-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2fce2-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="2fce2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fce2-102">SYNOPSIS</span></span>
<span data-ttu-id="2fce2-103">Ottiene i certificati di automazione.</span><span class="sxs-lookup"><span data-stu-id="2fce2-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="2fce2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fce2-104">SYNTAX</span></span>

### <span data-ttu-id="2fce2-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2fce2-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fce2-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="2fce2-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fce2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fce2-107">DESCRIPTION</span></span>
<span data-ttu-id="2fce2-108">Il cmdlet **Get-AzAutomationCertificate** ottiene uno o più certificati di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="2fce2-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="2fce2-109">Per impostazione predefinita, questo cmdlet ottiene tutti i certificati.</span><span class="sxs-lookup"><span data-stu-id="2fce2-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="2fce2-110">Specificare il nome di un certificato per ottenere un certificato specifico.</span><span class="sxs-lookup"><span data-stu-id="2fce2-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="2fce2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fce2-111">EXAMPLES</span></span>

### <span data-ttu-id="2fce2-112">Esempio 1: ottenere tutti i certificati</span><span class="sxs-lookup"><span data-stu-id="2fce2-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="2fce2-113">Questo comando consente di ottenere metadati per tutti i certificati nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2fce2-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="2fce2-114">Esempio 2: ottenere un certificato</span><span class="sxs-lookup"><span data-stu-id="2fce2-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="2fce2-115">Questo comando consente di ottenere metadati per il certificato denominato ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="2fce2-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="2fce2-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fce2-116">PARAMETERS</span></span>

### <span data-ttu-id="2fce2-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2fce2-117">-AutomationAccountName</span></span>
<span data-ttu-id="2fce2-118">Specifica il nome dell'account di automazione per cui questo cmdlet recupera un certificato.</span><span class="sxs-lookup"><span data-stu-id="2fce2-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="2fce2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fce2-119">-DefaultProfile</span></span>
<span data-ttu-id="2fce2-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2fce2-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fce2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fce2-121">-Name</span></span>
<span data-ttu-id="2fce2-122">Specifica il nome di un certificato da recuperare.</span><span class="sxs-lookup"><span data-stu-id="2fce2-122">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="2fce2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fce2-123">-ResourceGroupName</span></span>
<span data-ttu-id="2fce2-124">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="2fce2-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="2fce2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fce2-125">CommonParameters</span></span>
<span data-ttu-id="2fce2-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fce2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fce2-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fce2-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fce2-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fce2-128">INPUTS</span></span>

### <span data-ttu-id="2fce2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2fce2-129">System.String</span></span>

## <span data-ttu-id="2fce2-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fce2-130">OUTPUTS</span></span>

### <span data-ttu-id="2fce2-131">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="2fce2-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="2fce2-132">Note</span><span class="sxs-lookup"><span data-stu-id="2fce2-132">NOTES</span></span>

## <span data-ttu-id="2fce2-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fce2-133">RELATED LINKS</span></span>

[<span data-ttu-id="2fce2-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2fce2-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="2fce2-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2fce2-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="2fce2-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="2fce2-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


