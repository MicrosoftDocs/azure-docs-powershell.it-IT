---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FDA8BAAA-7C37-4BCB-9C02-EB6296C09C2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 00904cc1b67c32bc3658c1c4f6e8b123a5601ff7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029684"
---
# <span data-ttu-id="4fe90-101">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4fe90-101">New-AzureAutomationCertificate</span></span>

## <span data-ttu-id="4fe90-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4fe90-102">SYNOPSIS</span></span>

<span data-ttu-id="4fe90-103">Crea un certificato di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="4fe90-103">Creates an Azure Automation certificate.</span></span>

## <span data-ttu-id="4fe90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fe90-104">SYNTAX</span></span>

```
New-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>] -Path <String>
 [-Exportable] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4fe90-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fe90-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4fe90-106">Il cmdlet **New-AzureAutomationCertificate** crea un certificato in Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4fe90-106">The **New-AzureAutomationCertificate** cmdlet creates a certificate in Microsoft Azure Automation.</span></span>
<span data-ttu-id="4fe90-107">Si specifica il percorso di un file di certificato da caricare.</span><span class="sxs-lookup"><span data-stu-id="4fe90-107">You provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="4fe90-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fe90-108">EXAMPLES</span></span>

### <span data-ttu-id="4fe90-109">Esempio 1: creare un certificato</span><span class="sxs-lookup"><span data-stu-id="4fe90-109">Example 1: Create a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> New-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="4fe90-110">Questi comandi creano un certificato in Azure Automation denominato certificato.</span><span class="sxs-lookup"><span data-stu-id="4fe90-110">These commands create a certificate in Azure Automation named MyCertificate.</span></span>
<span data-ttu-id="4fe90-111">Il primo comando crea la password per il file di certificato usato nel secondo comando che crea il certificato.</span><span class="sxs-lookup"><span data-stu-id="4fe90-111">The first command creates the password for the certificate file that is used in the second command that creates the certificate.</span></span>

## <span data-ttu-id="4fe90-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4fe90-112">PARAMETERS</span></span>

### <span data-ttu-id="4fe90-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4fe90-113">-AutomationAccountName</span></span>
<span data-ttu-id="4fe90-114">Specifica il nome dell'account di automazione in cui verrà archiviato il certificato.</span><span class="sxs-lookup"><span data-stu-id="4fe90-114">Specifies the name of the Automation account the certificate will be stored in.</span></span>

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

### <span data-ttu-id="4fe90-115">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fe90-115">-Description</span></span>
<span data-ttu-id="4fe90-116">Specifica una descrizione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="4fe90-116">Specifies a description for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe90-117">-Esportabile</span><span class="sxs-lookup"><span data-stu-id="4fe90-117">-Exportable</span></span>
<span data-ttu-id="4fe90-118">Indica che il certificato può essere esportato.</span><span class="sxs-lookup"><span data-stu-id="4fe90-118">Indicates the certificate can be exported.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe90-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="4fe90-119">-Name</span></span>
<span data-ttu-id="4fe90-120">Specifica un nome per il certificato.</span><span class="sxs-lookup"><span data-stu-id="4fe90-120">Specifies a name for the certificate.</span></span>

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

### <span data-ttu-id="4fe90-121">-Password</span><span class="sxs-lookup"><span data-stu-id="4fe90-121">-Password</span></span>
<span data-ttu-id="4fe90-122">Specifica la password per il file di certificato.</span><span class="sxs-lookup"><span data-stu-id="4fe90-122">Specifies the password for the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe90-123">-Path</span><span class="sxs-lookup"><span data-stu-id="4fe90-123">-Path</span></span>
<span data-ttu-id="4fe90-124">Specifica il percorso di un file di script da caricare.</span><span class="sxs-lookup"><span data-stu-id="4fe90-124">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="4fe90-125">Il file può essere con estensione cer o PFX.</span><span class="sxs-lookup"><span data-stu-id="4fe90-125">The file can be .cer or .pfx.</span></span>

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

### <span data-ttu-id="4fe90-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="4fe90-126">-Profile</span></span>
<span data-ttu-id="4fe90-127">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fe90-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4fe90-128">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="4fe90-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4fe90-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe90-129">CommonParameters</span></span>
<span data-ttu-id="4fe90-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fe90-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe90-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fe90-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe90-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4fe90-132">INPUTS</span></span>

## <span data-ttu-id="4fe90-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fe90-133">OUTPUTS</span></span>

### <span data-ttu-id="4fe90-134">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="4fe90-134">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="4fe90-135">Note</span><span class="sxs-lookup"><span data-stu-id="4fe90-135">NOTES</span></span>

## <span data-ttu-id="4fe90-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fe90-136">RELATED LINKS</span></span>

[<span data-ttu-id="4fe90-137">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4fe90-137">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="4fe90-138">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4fe90-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="4fe90-139">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4fe90-139">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


