---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
ms.openlocfilehash: f68a7d29f71d51a25713310a1bf3288df316a34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686958"
---
# <span data-ttu-id="72189-101">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="72189-101">Get-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="72189-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72189-102">SYNOPSIS</span></span>
<span data-ttu-id="72189-103">Ottiene i certificati di automazione.</span><span class="sxs-lookup"><span data-stu-id="72189-103">Gets Automation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72189-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72189-104">SYNTAX</span></span>

### <span data-ttu-id="72189-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72189-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72189-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="72189-106">ByCertificateName</span></span>
```
Get-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72189-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72189-107">DESCRIPTION</span></span>
<span data-ttu-id="72189-108">Il cmdlet **Get-AzureRmAutomationCertificate** ottiene uno o più certificati di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="72189-108">The **Get-AzureRmAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="72189-109">Per impostazione predefinita, questo cmdlet ottiene tutti i certificati.</span><span class="sxs-lookup"><span data-stu-id="72189-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="72189-110">Specificare il nome di un certificato per ottenere un certificato specifico.</span><span class="sxs-lookup"><span data-stu-id="72189-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="72189-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72189-111">EXAMPLES</span></span>

### <span data-ttu-id="72189-112">Esempio 1: ottenere tutti i certificati</span><span class="sxs-lookup"><span data-stu-id="72189-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="72189-113">Questo comando consente di ottenere metadati per tutti i certificati nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="72189-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="72189-114">Esempio 2: ottenere un certificato</span><span class="sxs-lookup"><span data-stu-id="72189-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="72189-115">Questo comando consente di ottenere metadati per il certificato denominato ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="72189-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="72189-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72189-116">PARAMETERS</span></span>

### <span data-ttu-id="72189-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="72189-117">-AutomationAccountName</span></span>
<span data-ttu-id="72189-118">Specifica il nome dell'account di automazione per cui questo cmdlet recupera un certificato.</span><span class="sxs-lookup"><span data-stu-id="72189-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="72189-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72189-119">-DefaultProfile</span></span>
<span data-ttu-id="72189-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="72189-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72189-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="72189-121">-Name</span></span>
<span data-ttu-id="72189-122">Specifica il nome di un certificato da recuperare.</span><span class="sxs-lookup"><span data-stu-id="72189-122">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="72189-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72189-123">-ResourceGroupName</span></span>
<span data-ttu-id="72189-124">Specifica il nome di un gruppo di risorse per cui questo cmdlet ottiene un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="72189-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="72189-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72189-125">CommonParameters</span></span>
<span data-ttu-id="72189-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72189-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72189-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72189-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72189-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72189-128">INPUTS</span></span>

### <span data-ttu-id="72189-129">System. String</span><span class="sxs-lookup"><span data-stu-id="72189-129">System.String</span></span>

## <span data-ttu-id="72189-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72189-130">OUTPUTS</span></span>

### <span data-ttu-id="72189-131">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="72189-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="72189-132">Note</span><span class="sxs-lookup"><span data-stu-id="72189-132">NOTES</span></span>

## <span data-ttu-id="72189-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72189-133">RELATED LINKS</span></span>

[<span data-ttu-id="72189-134">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="72189-134">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="72189-135">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="72189-135">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="72189-136">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="72189-136">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


