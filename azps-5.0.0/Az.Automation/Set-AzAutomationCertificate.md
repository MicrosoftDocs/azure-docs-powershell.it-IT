---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCertificate.md
ms.openlocfilehash: 7eaaabf374d4ee9b43477596df06f58593c6d1e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202697"
---
# <span data-ttu-id="4464c-101">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4464c-101">Set-AzAutomationCertificate</span></span>

## <span data-ttu-id="4464c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4464c-102">SYNOPSIS</span></span>
<span data-ttu-id="4464c-103">Modifica la configurazione di un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="4464c-103">Modifies the configuration of an Automation certificate.</span></span>

## <span data-ttu-id="4464c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4464c-104">SYNTAX</span></span>

```
Set-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4464c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4464c-105">DESCRIPTION</span></span>
<span data-ttu-id="4464c-106">Il cmdlet **set-AzAutomationCertificate** modifica la configurazione di un certificato in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4464c-106">The **Set-AzAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="4464c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4464c-107">EXAMPLES</span></span>

### <span data-ttu-id="4464c-108">Esempio 1: modificare un certificato</span><span class="sxs-lookup"><span data-stu-id="4464c-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4464c-109">Il primo comando converte una password di testo normale in una stringa sicura usando il cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="4464c-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="4464c-110">Il comando Archivia l'oggetto nella variabile $Password.</span><span class="sxs-lookup"><span data-stu-id="4464c-110">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="4464c-111">Il secondo comando modifica un certificato denominato ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="4464c-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="4464c-112">Il comando usa la password archiviata in $Password.</span><span class="sxs-lookup"><span data-stu-id="4464c-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="4464c-113">Il comando specifica il nome dell'account e il percorso del file che viene caricato.</span><span class="sxs-lookup"><span data-stu-id="4464c-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="4464c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4464c-114">PARAMETERS</span></span>

### <span data-ttu-id="4464c-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4464c-115">-AutomationAccountName</span></span>
<span data-ttu-id="4464c-116">Specifica il nome dell'account di automazione per cui questo cmdlet modifica un certificato.</span><span class="sxs-lookup"><span data-stu-id="4464c-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="4464c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4464c-117">-DefaultProfile</span></span>
<span data-ttu-id="4464c-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4464c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4464c-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="4464c-119">-Description</span></span>
<span data-ttu-id="4464c-120">Specifica una descrizione per il certificato modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4464c-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4464c-121">-Esportabile</span><span class="sxs-lookup"><span data-stu-id="4464c-121">-Exportable</span></span>
<span data-ttu-id="4464c-122">Specifica se il certificato può essere esportato.</span><span class="sxs-lookup"><span data-stu-id="4464c-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="4464c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="4464c-123">-Name</span></span>
<span data-ttu-id="4464c-124">Specifica il nome del certificato modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4464c-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4464c-125">-Password</span><span class="sxs-lookup"><span data-stu-id="4464c-125">-Password</span></span>
<span data-ttu-id="4464c-126">Specifica la password per il file di certificato.</span><span class="sxs-lookup"><span data-stu-id="4464c-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="4464c-127">-Path</span><span class="sxs-lookup"><span data-stu-id="4464c-127">-Path</span></span>
<span data-ttu-id="4464c-128">Specifica il percorso di un file di script da caricare.</span><span class="sxs-lookup"><span data-stu-id="4464c-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="4464c-129">Il file può essere un file con estensione cer o un file PFX.</span><span class="sxs-lookup"><span data-stu-id="4464c-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="4464c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4464c-130">-ResourceGroupName</span></span>
<span data-ttu-id="4464c-131">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un certificato.</span><span class="sxs-lookup"><span data-stu-id="4464c-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

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

### <span data-ttu-id="4464c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4464c-132">CommonParameters</span></span>
<span data-ttu-id="4464c-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4464c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4464c-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4464c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4464c-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4464c-135">INPUTS</span></span>

### <span data-ttu-id="4464c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4464c-136">System.String</span></span>

### <span data-ttu-id="4464c-137">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="4464c-137">System.Security.SecureString</span></span>

### <span data-ttu-id="4464c-138">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4464c-138">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4464c-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4464c-139">OUTPUTS</span></span>

### <span data-ttu-id="4464c-140">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="4464c-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="4464c-141">Note</span><span class="sxs-lookup"><span data-stu-id="4464c-141">NOTES</span></span>

## <span data-ttu-id="4464c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4464c-142">RELATED LINKS</span></span>

[<span data-ttu-id="4464c-143">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4464c-143">Get-AzAutomationCertificate</span></span>](./Get-AzAutomationCertificate.md)

[<span data-ttu-id="4464c-144">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4464c-144">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="4464c-145">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="4464c-145">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)


