---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
ms.openlocfilehash: 83ec5c8cd9dd9937ca372441d5a9be005bffc76a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513967"
---
# <span data-ttu-id="63f33-101">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="63f33-101">New-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="63f33-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63f33-102">SYNOPSIS</span></span>
<span data-ttu-id="63f33-103">Crea un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="63f33-103">Creates an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63f33-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63f33-104">SYNTAX</span></span>

```
New-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63f33-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63f33-105">DESCRIPTION</span></span>
<span data-ttu-id="63f33-106">Il cmdlet **New-AzureRmAutomationCertificate** crea un certificato in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="63f33-106">The **New-AzureRmAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="63f33-107">Specificare il percorso di un file di certificato da caricare.</span><span class="sxs-lookup"><span data-stu-id="63f33-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="63f33-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63f33-108">EXAMPLES</span></span>

### <span data-ttu-id="63f33-109">Esempio 1: creare un nuovo certificato</span><span class="sxs-lookup"><span data-stu-id="63f33-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="63f33-110">Il primo comando converte una password di testo normale in una stringa sicura usando il cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="63f33-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="63f33-111">Il comando Archivia l'oggetto nella variabile $Password.</span><span class="sxs-lookup"><span data-stu-id="63f33-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="63f33-112">Il secondo comando crea un certificato denominato ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="63f33-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="63f33-113">Il comando usa la password archiviata in $Password.</span><span class="sxs-lookup"><span data-stu-id="63f33-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="63f33-114">Il comando specifica il nome dell'account e il percorso del file che viene caricato.</span><span class="sxs-lookup"><span data-stu-id="63f33-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="63f33-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63f33-115">PARAMETERS</span></span>

### <span data-ttu-id="63f33-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="63f33-116">-AutomationAccountName</span></span>
<span data-ttu-id="63f33-117">Specifica il nome dell'account di automazione per il quale questo cmdlet archivia il certificato.</span><span class="sxs-lookup"><span data-stu-id="63f33-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="63f33-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f33-118">-DefaultProfile</span></span>
<span data-ttu-id="63f33-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="63f33-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63f33-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="63f33-120">-Description</span></span>
<span data-ttu-id="63f33-121">Specifica una descrizione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="63f33-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="63f33-122">-Esportabile</span><span class="sxs-lookup"><span data-stu-id="63f33-122">-Exportable</span></span>
<span data-ttu-id="63f33-123">Specifica se il certificato può essere esportato.</span><span class="sxs-lookup"><span data-stu-id="63f33-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="63f33-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="63f33-124">-Name</span></span>
<span data-ttu-id="63f33-125">Specifica il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="63f33-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="63f33-126">-Password</span><span class="sxs-lookup"><span data-stu-id="63f33-126">-Password</span></span>
<span data-ttu-id="63f33-127">Specifica la password per il file di certificato.</span><span class="sxs-lookup"><span data-stu-id="63f33-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="63f33-128">-Path</span><span class="sxs-lookup"><span data-stu-id="63f33-128">-Path</span></span>
<span data-ttu-id="63f33-129">Specifica il percorso di un file di script caricato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63f33-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="63f33-130">Il file può essere un file con estensione cer o PFX.</span><span class="sxs-lookup"><span data-stu-id="63f33-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="63f33-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63f33-131">-ResourceGroupName</span></span>
<span data-ttu-id="63f33-132">Specifica il nome del gruppo di risorse per cui questo cmdlet crea un certificato.</span><span class="sxs-lookup"><span data-stu-id="63f33-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="63f33-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f33-133">CommonParameters</span></span>
<span data-ttu-id="63f33-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f33-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f33-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63f33-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f33-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63f33-136">INPUTS</span></span>

### <span data-ttu-id="63f33-137">System. String</span><span class="sxs-lookup"><span data-stu-id="63f33-137">System.String</span></span>

### <span data-ttu-id="63f33-138">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="63f33-138">System.Security.SecureString</span></span>

### <span data-ttu-id="63f33-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="63f33-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="63f33-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63f33-140">OUTPUTS</span></span>

### <span data-ttu-id="63f33-141">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="63f33-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="63f33-142">Note</span><span class="sxs-lookup"><span data-stu-id="63f33-142">NOTES</span></span>

## <span data-ttu-id="63f33-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63f33-143">RELATED LINKS</span></span>

[<span data-ttu-id="63f33-144">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="63f33-144">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="63f33-145">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="63f33-145">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="63f33-146">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="63f33-146">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


