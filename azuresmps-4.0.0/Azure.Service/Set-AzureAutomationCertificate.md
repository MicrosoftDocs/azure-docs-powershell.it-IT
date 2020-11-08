---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: AE74024A-A12A-4EC4-AF6C-62F921EA2532
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b19d0bb0c95e9d489fe26c1cd74705318cedcf2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029890"
---
# <span data-ttu-id="01692-101">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="01692-101">Set-AzureAutomationCertificate</span></span>

## <span data-ttu-id="01692-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01692-102">SYNOPSIS</span></span>

<span data-ttu-id="01692-103">Modifica la configurazione di un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="01692-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="01692-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01692-104">SYNTAX</span></span>

```
Set-AzureAutomationCertificate -Name <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="01692-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01692-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="01692-106">Il cmdlet **set-AzureAutomationCertificate** modifica la configurazione di un certificato in Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="01692-106">The **Set-AzureAutomationCertificate** cmdlet modifies the configuration of a certificate in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="01692-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01692-107">EXAMPLES</span></span>

### <span data-ttu-id="01692-108">Esempio 1: aggiornare un certificato</span><span class="sxs-lookup"><span data-stu-id="01692-108">Example 1: Update a certificate</span></span>
```
PS C:\> $password = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "MyCertificate" -Path "./cert.pfx" -Password $password
```

<span data-ttu-id="01692-109">Questi comandi aggiornano un certificato esistente denominato certificato in automazione.</span><span class="sxs-lookup"><span data-stu-id="01692-109">These commands update an existing certificate named MyCertificate in Automation.</span></span>
<span data-ttu-id="01692-110">Il primo comando crea la password per il file di certificato usato nel secondo comando che aggiorna il certificato.</span><span class="sxs-lookup"><span data-stu-id="01692-110">The first command creates the password for the certificate file that is used in the second command that updates the certificate.</span></span>

## <span data-ttu-id="01692-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01692-111">PARAMETERS</span></span>

### <span data-ttu-id="01692-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="01692-112">-AutomationAccountName</span></span>
<span data-ttu-id="01692-113">Specifica il nome dell'account di automazione con il certificato.</span><span class="sxs-lookup"><span data-stu-id="01692-113">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="01692-114">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="01692-114">-Description</span></span>
<span data-ttu-id="01692-115">Specifica una descrizione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="01692-115">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="01692-116">-Esportabile</span><span class="sxs-lookup"><span data-stu-id="01692-116">-Exportable</span></span>
<span data-ttu-id="01692-117">Indica che il certificato può essere esportato.</span><span class="sxs-lookup"><span data-stu-id="01692-117">Indicates the certificate can be exported.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01692-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="01692-118">-Name</span></span>
<span data-ttu-id="01692-119">Specifica il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="01692-119">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="01692-120">-Password</span><span class="sxs-lookup"><span data-stu-id="01692-120">-Password</span></span>
<span data-ttu-id="01692-121">Specifica la password per il file di certificato.</span><span class="sxs-lookup"><span data-stu-id="01692-121">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="01692-122">-Path</span><span class="sxs-lookup"><span data-stu-id="01692-122">-Path</span></span>
<span data-ttu-id="01692-123">Specifica il percorso di un file di script da caricare.</span><span class="sxs-lookup"><span data-stu-id="01692-123">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="01692-124">Il file può essere con estensione cer o PFX.</span><span class="sxs-lookup"><span data-stu-id="01692-124">The file can be .cer or .pfx.</span></span>

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

### <span data-ttu-id="01692-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="01692-125">-Profile</span></span>
<span data-ttu-id="01692-126">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01692-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="01692-127">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="01692-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="01692-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01692-128">CommonParameters</span></span>
<span data-ttu-id="01692-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01692-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01692-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01692-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01692-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01692-131">INPUTS</span></span>

## <span data-ttu-id="01692-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01692-132">OUTPUTS</span></span>

### <span data-ttu-id="01692-133">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="01692-133">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="01692-134">Note</span><span class="sxs-lookup"><span data-stu-id="01692-134">NOTES</span></span>

## <span data-ttu-id="01692-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01692-135">RELATED LINKS</span></span>

[<span data-ttu-id="01692-136">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="01692-136">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="01692-137">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="01692-137">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="01692-138">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="01692-138">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)


