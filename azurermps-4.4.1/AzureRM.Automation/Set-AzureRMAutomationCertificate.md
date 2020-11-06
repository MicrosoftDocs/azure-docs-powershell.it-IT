---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
ms.openlocfilehash: 97a5db6a816b2274befde1d4efb898b0c5e2bfdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522000"
---
# <span data-ttu-id="390e2-101">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="390e2-101">Set-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="390e2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="390e2-102">SYNOPSIS</span></span>
<span data-ttu-id="390e2-103">Modifica la configurazione di un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="390e2-103">Modifies the configuration of an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="390e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="390e2-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="390e2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="390e2-105">DESCRIPTION</span></span>
<span data-ttu-id="390e2-106">Il cmdlet **set-AzureRmAutomationCertificate** modifica la configurazione di un certificato in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="390e2-106">The **Set-AzureRmAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="390e2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="390e2-107">EXAMPLES</span></span>

### <span data-ttu-id="390e2-108">Esempio 1: modificare un certificato</span><span class="sxs-lookup"><span data-stu-id="390e2-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="390e2-109">Il primo comando converte una password di testo normale in una stringa sicura usando il cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="390e2-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="390e2-110">Il comando Archivia l'oggetto nella variabile $Password.</span><span class="sxs-lookup"><span data-stu-id="390e2-110">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="390e2-111">Il secondo comando modifica un certificato denominato ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="390e2-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="390e2-112">Il comando usa la password archiviata in $Password.</span><span class="sxs-lookup"><span data-stu-id="390e2-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="390e2-113">Il comando specifica il nome dell'account e il percorso del file che viene caricato.</span><span class="sxs-lookup"><span data-stu-id="390e2-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="390e2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="390e2-114">PARAMETERS</span></span>

### <span data-ttu-id="390e2-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="390e2-115">-AutomationAccountName</span></span>
<span data-ttu-id="390e2-116">Specifica il nome dell'account di automazione per cui questo cmdlet modifica un certificato.</span><span class="sxs-lookup"><span data-stu-id="390e2-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="390e2-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="390e2-117">-Description</span></span>
<span data-ttu-id="390e2-118">Specifica una descrizione per il certificato modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="390e2-118">Specifies a description for the certificate that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="390e2-119">-Esportabile</span><span class="sxs-lookup"><span data-stu-id="390e2-119">-Exportable</span></span>
<span data-ttu-id="390e2-120">Specifica se il certificato può essere esportato.</span><span class="sxs-lookup"><span data-stu-id="390e2-120">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="390e2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="390e2-121">-Name</span></span>
<span data-ttu-id="390e2-122">Specifica il nome del certificato modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="390e2-122">Specifies the name of the certificate that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="390e2-123">-Password</span><span class="sxs-lookup"><span data-stu-id="390e2-123">-Password</span></span>
<span data-ttu-id="390e2-124">Specifica la password per il file di certificato.</span><span class="sxs-lookup"><span data-stu-id="390e2-124">Specifies the password for the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="390e2-125">-Path</span><span class="sxs-lookup"><span data-stu-id="390e2-125">-Path</span></span>
<span data-ttu-id="390e2-126">Specifica il percorso di un file di script da caricare.</span><span class="sxs-lookup"><span data-stu-id="390e2-126">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="390e2-127">Il file può essere un file con estensione cer o un file PFX.</span><span class="sxs-lookup"><span data-stu-id="390e2-127">The file can be a .cer file or a .pfx file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="390e2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="390e2-128">-ResourceGroupName</span></span>
<span data-ttu-id="390e2-129">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un certificato.</span><span class="sxs-lookup"><span data-stu-id="390e2-129">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="390e2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="390e2-130">-DefaultProfile</span></span>
<span data-ttu-id="390e2-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="390e2-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="390e2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="390e2-132">CommonParameters</span></span>
<span data-ttu-id="390e2-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="390e2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="390e2-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="390e2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="390e2-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="390e2-135">INPUTS</span></span>

## <span data-ttu-id="390e2-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="390e2-136">OUTPUTS</span></span>

### <span data-ttu-id="390e2-137">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="390e2-137">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="390e2-138">Note</span><span class="sxs-lookup"><span data-stu-id="390e2-138">NOTES</span></span>

## <span data-ttu-id="390e2-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="390e2-139">RELATED LINKS</span></span>

[<span data-ttu-id="390e2-140">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="390e2-140">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="390e2-141">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="390e2-141">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="390e2-142">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="390e2-142">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)


