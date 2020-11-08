---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FED10AA9-DD3A-4034-B78E-F9E55290B353
online version: ''
schema: 2.0.0
ms.openlocfilehash: 272969751988d3747788c2a214e8eb7ed509f232
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023621"
---
# <span data-ttu-id="1a69b-101">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1a69b-101">Get-AzureAutomationCertificate</span></span>

## <span data-ttu-id="1a69b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a69b-102">SYNOPSIS</span></span>

<span data-ttu-id="1a69b-103">Ottiene un certificato di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1a69b-103">Gets an Azure Automation certificate.</span></span>

## <span data-ttu-id="1a69b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a69b-104">SYNTAX</span></span>

### <span data-ttu-id="1a69b-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1a69b-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCertificate -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1a69b-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="1a69b-106">ByCertificateName</span></span>
```
Get-AzureAutomationCertificate -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a69b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a69b-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1a69b-108">Il cmdlet **Get-AzureAutomationCertificate** ottiene uno o più certificati di automazione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1a69b-108">The **Get-AzureAutomationCertificate** cmdlet gets one or more Microsoft Azure Automation certificates.</span></span>
<span data-ttu-id="1a69b-109">Per impostazione predefinita, vengono restituiti tutti i certificati.</span><span class="sxs-lookup"><span data-stu-id="1a69b-109">By default, all certificates are returned.</span></span>
<span data-ttu-id="1a69b-110">Per ottenere un certificato specifico, specificarne il nome.</span><span class="sxs-lookup"><span data-stu-id="1a69b-110">To get a specific certificate, specify its name.</span></span>

## <span data-ttu-id="1a69b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a69b-111">EXAMPLES</span></span>

### <span data-ttu-id="1a69b-112">Esempio 1: ottenere tutti i certificati</span><span class="sxs-lookup"><span data-stu-id="1a69b-112">Example 1: Get all certificates</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17"
```

<span data-ttu-id="1a69b-113">Questo comando consente di ottenere tutti i certificati nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1a69b-113">This command gets all certificates in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="1a69b-114">Esempio 2: ottenere un certificato</span><span class="sxs-lookup"><span data-stu-id="1a69b-114">Example 2: Get a certificate</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyUserCertificate"
```

<span data-ttu-id="1a69b-115">Questo comando ottiene il certificato denominato MyUserCertificate.</span><span class="sxs-lookup"><span data-stu-id="1a69b-115">This command gets the certificate named MyUserCertificate.</span></span>

## <span data-ttu-id="1a69b-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a69b-116">PARAMETERS</span></span>

### <span data-ttu-id="1a69b-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1a69b-117">-AutomationAccountName</span></span>
<span data-ttu-id="1a69b-118">Specifica il nome dell'account di automazione con il certificato.</span><span class="sxs-lookup"><span data-stu-id="1a69b-118">Specifies the name of the automation account with the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a69b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a69b-119">-Name</span></span>
<span data-ttu-id="1a69b-120">Specifica il nome di un certificato da recuperare.</span><span class="sxs-lookup"><span data-stu-id="1a69b-120">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a69b-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="1a69b-121">-Profile</span></span>
<span data-ttu-id="1a69b-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a69b-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1a69b-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1a69b-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a69b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a69b-124">CommonParameters</span></span>
<span data-ttu-id="1a69b-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a69b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a69b-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a69b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a69b-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a69b-127">INPUTS</span></span>

## <span data-ttu-id="1a69b-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a69b-128">OUTPUTS</span></span>

### <span data-ttu-id="1a69b-129">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="1a69b-129">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="1a69b-130">Note</span><span class="sxs-lookup"><span data-stu-id="1a69b-130">NOTES</span></span>

## <span data-ttu-id="1a69b-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a69b-131">RELATED LINKS</span></span>

[<span data-ttu-id="1a69b-132">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1a69b-132">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="1a69b-133">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1a69b-133">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="1a69b-134">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="1a69b-134">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


