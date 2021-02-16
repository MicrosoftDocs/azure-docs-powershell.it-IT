---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 7eaaabf374d4ee9b43477596df06f58593c6d1e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199614"
---
# <span data-ttu-id="6c0fe-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6c0fe-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="6c0fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c0fe-102">SYNOPSIS</span></span>
<span data-ttu-id="6c0fe-103">Modifica la configurazione di un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="6c0fe-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="6c0fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c0fe-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c0fe-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6c0fe-105">DESCRIPTION</span></span>
<span data-ttu-id="6c0fe-106">Il cmdlet **Set-AzAutomationCertificate** modifica la configurazione di un certificato nell'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6c0fe-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="6c0fe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c0fe-107">EXAMPLES</span></span>

### <span data-ttu-id="6c0fe-108">Esempio 1: Modificare un certificato</span><span class="sxs-lookup"><span data-stu-id="6c0fe-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6c0fe-109">Il primo comando converte una password di testo normale in una stringa sicura usando il cmdlet ConvertTo-SecureString testo.</span><span class="sxs-lookup"><span data-stu-id="6c0fe-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="6c0fe-110">Il comando archivia l'oggetto nella $Password variabile.</span><span class="sxs-lookup"><span data-stu-id="6c0fe-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="6c0fe-111">Il secondo comando modifica un certificato denominato ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="6c0fe-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="6c0fe-112">Il comando usa la password archiviata in $Password.</span><span class="sxs-lookup"><span data-stu-id="6c0fe-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="6c0fe-113">Il comando specifica il nome dell'account e il percorso del file caricato.</span><span class="sxs-lookup"><span data-stu-id="6c0fe-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="6c0fe-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c0fe-114">PARAMETERS</span></span>

### <span data-ttu-id="6c0fe-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6c0fe-115">-AutomationAccountName</span></span>
<span data-ttu-id="6c0fe-116">Specifica il nome dell'account di automazione per cui questo cmdlet modifica un certificato.</span><span class="sxs-lookup"><span data-stu-id="6c0fe-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="6c0fe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c0fe-117">-DefaultProfile</span></span>
<span data-ttu-id="6c0fe-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="6c0fe-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c0fe-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c0fe-119">-Description</span></span>
<span data-ttu-id="6c0fe-120">Specifica una descrizione per il certificato modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c0fe-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6c0fe-121">-Esportabile</span><span class="sxs-lookup"><span data-stu-id="6c0fe-121">-Exportable</span></span>
<span data-ttu-id="6c0fe-122">Specifica se il certificato può essere esportato.</span><span class="sxs-lookup"><span data-stu-id="6c0fe-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="6c0fe-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6c0fe-123">-Name</span></span>
<span data-ttu-id="6c0fe-124">Specifica il nome del certificato modificato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c0fe-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="6c0fe-125">-Password</span><span class="sxs-lookup"><span data-stu-id="6c0fe-125">-Password</span></span>
<span data-ttu-id="6c0fe-126">Specifica la password per il file di certificato.</span><span class="sxs-lookup"><span data-stu-id="6c0fe-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="6c0fe-127">-Path</span><span class="sxs-lookup"><span data-stu-id="6c0fe-127">-Path</span></span>
<span data-ttu-id="6c0fe-128">Specifica il percorso di un file script da caricare.</span><span class="sxs-lookup"><span data-stu-id="6c0fe-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="6c0fe-129">Il file può essere con estensione cer o pfx.</span><span class="sxs-lookup"><span data-stu-id="6c0fe-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="6c0fe-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c0fe-130">-ResourceGroupName</span></span>
<span data-ttu-id="6c0fe-131">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un certificato.</span><span class="sxs-lookup"><span data-stu-id="6c0fe-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="6c0fe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c0fe-132">CommonParameters</span></span>
<span data-ttu-id="6c0fe-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c0fe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c0fe-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c0fe-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c0fe-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="6c0fe-135">INPUTS</span></span>

### <span data-ttu-id="6c0fe-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6c0fe-136">System.String</span></span>

### <span data-ttu-id="6c0fe-137">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="6c0fe-137">System.Security.SecureString</span></span>

### <span data-ttu-id="6c0fe-138">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6c0fe-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6c0fe-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c0fe-139">OUTPUTS</span></span>

### <span data-ttu-id="6c0fe-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="6c0fe-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="6c0fe-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="6c0fe-141">NOTES</span></span>

## <span data-ttu-id="6c0fe-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c0fe-142">RELATED LINKS</span></span>

[<span data-ttu-id="6c0fe-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6c0fe-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="6c0fe-144">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6c0fe-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="6c0fe-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="6c0fe-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


