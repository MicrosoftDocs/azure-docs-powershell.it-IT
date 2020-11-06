---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
ms.openlocfilehash: a3e662d031c036686298beaa5c80bd4efa8a3888
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517120"
---
# <span data-ttu-id="f520b-101">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f520b-101">New-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="f520b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f520b-102">SYNOPSIS</span></span>
<span data-ttu-id="f520b-103">Crea un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="f520b-103">Creates an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f520b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f520b-104">SYNTAX</span></span>

```
New-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f520b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f520b-105">DESCRIPTION</span></span>
<span data-ttu-id="f520b-106">Il cmdlet **New-AzureRmAutomationCertificate** crea un certificato in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f520b-106">The **New-AzureRmAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="f520b-107">Specificare il percorso di un file di certificato da caricare.</span><span class="sxs-lookup"><span data-stu-id="f520b-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="f520b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f520b-108">EXAMPLES</span></span>

### <span data-ttu-id="f520b-109">Esempio 1: creare un nuovo certificato</span><span class="sxs-lookup"><span data-stu-id="f520b-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f520b-110">Il primo comando converte una password di testo normale in una stringa sicura usando il cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="f520b-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="f520b-111">Il comando Archivia l'oggetto nella variabile $Password.</span><span class="sxs-lookup"><span data-stu-id="f520b-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="f520b-112">Il secondo comando crea un certificato denominato ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="f520b-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="f520b-113">Il comando usa la password archiviata in $Password.</span><span class="sxs-lookup"><span data-stu-id="f520b-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="f520b-114">Il comando specifica il nome dell'account e il percorso del file che viene caricato.</span><span class="sxs-lookup"><span data-stu-id="f520b-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="f520b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f520b-115">PARAMETERS</span></span>

### <span data-ttu-id="f520b-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f520b-116">-AutomationAccountName</span></span>
<span data-ttu-id="f520b-117">Specifica il nome dell'account di automazione per il quale questo cmdlet archivia il certificato.</span><span class="sxs-lookup"><span data-stu-id="f520b-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="f520b-118">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f520b-118">-Description</span></span>
<span data-ttu-id="f520b-119">Specifica una descrizione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="f520b-119">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="f520b-120">-Esportabile</span><span class="sxs-lookup"><span data-stu-id="f520b-120">-Exportable</span></span>
<span data-ttu-id="f520b-121">Specifica se il certificato può essere esportato.</span><span class="sxs-lookup"><span data-stu-id="f520b-121">Specifies whether the certificate can be exported.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f520b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f520b-122">-Name</span></span>
<span data-ttu-id="f520b-123">Specifica il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="f520b-123">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="f520b-124">-Password</span><span class="sxs-lookup"><span data-stu-id="f520b-124">-Password</span></span>
<span data-ttu-id="f520b-125">Specifica la password per il file di certificato.</span><span class="sxs-lookup"><span data-stu-id="f520b-125">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="f520b-126">-Path</span><span class="sxs-lookup"><span data-stu-id="f520b-126">-Path</span></span>
<span data-ttu-id="f520b-127">Specifica il percorso di un file di script caricato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f520b-127">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="f520b-128">Il file può essere un file con estensione cer o PFX.</span><span class="sxs-lookup"><span data-stu-id="f520b-128">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="f520b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f520b-129">-ResourceGroupName</span></span>
<span data-ttu-id="f520b-130">Specifica il nome del gruppo di risorse per cui questo cmdlet crea un certificato.</span><span class="sxs-lookup"><span data-stu-id="f520b-130">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="f520b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f520b-131">-DefaultProfile</span></span>
<span data-ttu-id="f520b-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f520b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f520b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f520b-133">CommonParameters</span></span>
<span data-ttu-id="f520b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f520b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f520b-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f520b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f520b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f520b-136">INPUTS</span></span>

## <span data-ttu-id="f520b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f520b-137">OUTPUTS</span></span>

### <span data-ttu-id="f520b-138">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="f520b-138">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="f520b-139">Note</span><span class="sxs-lookup"><span data-stu-id="f520b-139">NOTES</span></span>

## <span data-ttu-id="f520b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f520b-140">RELATED LINKS</span></span>

[<span data-ttu-id="f520b-141">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f520b-141">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="f520b-142">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f520b-142">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="f520b-143">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f520b-143">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


