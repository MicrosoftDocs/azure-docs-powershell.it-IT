---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: 3f92ebfcb9b768788b0a9acd7a1e11ef766fd22b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010909"
---
# <span data-ttu-id="3e3f4-101">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3e3f4-101">New-AzAutomationCertificate</span></span>

## <span data-ttu-id="3e3f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="3e3f4-103">Crea un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-103">Creates an Automation certificate.</span></span>

## <span data-ttu-id="3e3f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e3f4-104">SYNTAX</span></span>

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e3f4-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3e3f4-105">DESCRIPTION</span></span>
<span data-ttu-id="3e3f4-106">Il cmdlet **New-AzAutomationCertificate** crea un certificato nell'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-106">The **New-AzAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="3e3f4-107">Specificare il percorso di un file di certificato da caricare.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="3e3f4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e3f4-108">EXAMPLES</span></span>

### <span data-ttu-id="3e3f4-109">Esempio 1: Creare un nuovo certificato</span><span class="sxs-lookup"><span data-stu-id="3e3f4-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3e3f4-110">Il primo comando converte una password di testo normale in una stringa sicura usando il cmdlet ConvertTo-SecureString testo.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="3e3f4-111">Il comando archivia l'oggetto nella $Password variabile.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="3e3f4-112">Il secondo comando crea un certificato denominato ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="3e3f4-113">Il comando usa la password archiviata in $Password.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="3e3f4-114">Il comando specifica il nome dell'account e il percorso del file da caricare.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="3e3f4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e3f4-115">PARAMETERS</span></span>

### <span data-ttu-id="3e3f4-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3e3f4-116">-AutomationAccountName</span></span>
<span data-ttu-id="3e3f4-117">Specifica il nome dell'account di automazione per cui questo cmdlet archivia il certificato.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="3e3f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e3f4-118">-DefaultProfile</span></span>
<span data-ttu-id="3e3f4-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3e3f4-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e3f4-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e3f4-120">-Description</span></span>
<span data-ttu-id="3e3f4-121">Specifica una descrizione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="3e3f4-122">-Esportabile</span><span class="sxs-lookup"><span data-stu-id="3e3f4-122">-Exportable</span></span>
<span data-ttu-id="3e3f4-123">Specifica se il certificato può essere esportato.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="3e3f4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3e3f4-124">-Name</span></span>
<span data-ttu-id="3e3f4-125">Specifica il nome per il certificato.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="3e3f4-126">-Password</span><span class="sxs-lookup"><span data-stu-id="3e3f4-126">-Password</span></span>
<span data-ttu-id="3e3f4-127">Specifica la password per il file di certificato.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="3e3f4-128">-Path</span><span class="sxs-lookup"><span data-stu-id="3e3f4-128">-Path</span></span>
<span data-ttu-id="3e3f4-129">Specifica il percorso di un file script caricato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="3e3f4-130">Il file può essere con estensione cer o pfx.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="3e3f4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e3f4-131">-ResourceGroupName</span></span>
<span data-ttu-id="3e3f4-132">Specifica il nome del gruppo di risorse per cui questo cmdlet crea un certificato.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="3e3f4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e3f4-133">CommonParameters</span></span>
<span data-ttu-id="3e3f4-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e3f4-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e3f4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e3f4-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="3e3f4-136">INPUTS</span></span>

### <span data-ttu-id="3e3f4-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3e3f4-137">System.String</span></span>

### <span data-ttu-id="3e3f4-138">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="3e3f4-138">System.Security.SecureString</span></span>

### <span data-ttu-id="3e3f4-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3e3f4-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3e3f4-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e3f4-140">OUTPUTS</span></span>

### <span data-ttu-id="3e3f4-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="3e3f4-141">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="3e3f4-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="3e3f4-142">NOTES</span></span>

<span data-ttu-id="3e3f4-143">Questo comando deve essere eseguito in un computer di cui si è amministratori e in una sessione di PowerShell con privilegi elevati. prima del caricamento del certificato, questo cmdlet usa l'archivio X.509 locale per recuperare l'immagine thumbprint e la chiave e, se il cmdlet viene eseguito all'esterno di una sessione di PowerShell con privilegi elevati, viene visualizzato un errore di accesso negato.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-143">This command should be run on a machine that you are an administrator of, as well as in an elevated PowerShell session; before the certificate is uploaded, this cmdlet uses the local X.509 store to retrieve the thumbprint and key, and if this cmdlet is run outside of an elevated PowerShell session, you will receive an "Access denied" error.</span></span>

## <span data-ttu-id="3e3f4-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e3f4-144">RELATED LINKS</span></span>

[<span data-ttu-id="3e3f4-145">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3e3f4-145">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="3e3f4-146">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3e3f4-146">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="3e3f4-147">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3e3f4-147">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


