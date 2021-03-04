---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 80a33fe4664e4c7814db6774e7cd427dd9a2c87e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957726"
---
# <span data-ttu-id="d0096-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d0096-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="d0096-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0096-102">SYNOPSIS</span></span>
<span data-ttu-id="d0096-103">Modifica la configurazione di un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="d0096-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="d0096-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0096-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0096-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d0096-105">DESCRIPTION</span></span>
<span data-ttu-id="d0096-106">Il cmdlet **Set-AzAutomationCertificate** modifica la configurazione di un certificato nell'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d0096-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="d0096-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0096-107">EXAMPLES</span></span>

### <span data-ttu-id="d0096-108">Esempio 1: Modificare un certificato</span><span class="sxs-lookup"><span data-stu-id="d0096-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d0096-109">Il primo comando converte una password di testo normale in stringa sicura usando il cmdlet ConvertTo-SecureString testo.</span><span class="sxs-lookup"><span data-stu-id="d0096-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="d0096-110">Il comando archivia l'oggetto nella $Password variabile.</span><span class="sxs-lookup"><span data-stu-id="d0096-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="d0096-111">Il secondo comando modifica un certificato denominato ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="d0096-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="d0096-112">Il comando usa la password archiviata in $Password.</span><span class="sxs-lookup"><span data-stu-id="d0096-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="d0096-113">Il comando specifica il nome dell'account e il percorso del file da caricare.</span><span class="sxs-lookup"><span data-stu-id="d0096-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="d0096-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0096-114">PARAMETERS</span></span>

### <span data-ttu-id="d0096-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d0096-115">-AutomationAccountName</span></span>
<span data-ttu-id="d0096-116">Specifica il nome dell'account di automazione per cui questo cmdlet modifica un certificato.</span><span class="sxs-lookup"><span data-stu-id="d0096-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="d0096-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0096-117">-DefaultProfile</span></span>
<span data-ttu-id="d0096-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d0096-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0096-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0096-119">-Description</span></span>
<span data-ttu-id="d0096-120">Specifica una descrizione per il certificato modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0096-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d0096-121">-Esportabile</span><span class="sxs-lookup"><span data-stu-id="d0096-121">-Exportable</span></span>
<span data-ttu-id="d0096-122">Specifica se il certificato può essere esportato.</span><span class="sxs-lookup"><span data-stu-id="d0096-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="d0096-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d0096-123">-Name</span></span>
<span data-ttu-id="d0096-124">Specifica il nome del certificato modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0096-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d0096-125">-Password</span><span class="sxs-lookup"><span data-stu-id="d0096-125">-Password</span></span>
<span data-ttu-id="d0096-126">Specifica la password per il file di certificato.</span><span class="sxs-lookup"><span data-stu-id="d0096-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="d0096-127">-Path</span><span class="sxs-lookup"><span data-stu-id="d0096-127">-Path</span></span>
<span data-ttu-id="d0096-128">Specifica il percorso di un file script da caricare.</span><span class="sxs-lookup"><span data-stu-id="d0096-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="d0096-129">Il file può essere un file con estensione cer o pfx.</span><span class="sxs-lookup"><span data-stu-id="d0096-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="d0096-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0096-130">-ResourceGroupName</span></span>
<span data-ttu-id="d0096-131">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un certificato.</span><span class="sxs-lookup"><span data-stu-id="d0096-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="d0096-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0096-132">CommonParameters</span></span>
<span data-ttu-id="d0096-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0096-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0096-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0096-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0096-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="d0096-135">INPUTS</span></span>

### <span data-ttu-id="d0096-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d0096-136">System.String</span></span>

### <span data-ttu-id="d0096-137">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="d0096-137">System.Security.SecureString</span></span>

### <span data-ttu-id="d0096-138">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d0096-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d0096-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0096-139">OUTPUTS</span></span>

### <span data-ttu-id="d0096-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="d0096-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="d0096-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="d0096-141">NOTES</span></span>

## <span data-ttu-id="d0096-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0096-142">RELATED LINKS</span></span>

[<span data-ttu-id="d0096-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d0096-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="d0096-144">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d0096-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="d0096-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="d0096-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


