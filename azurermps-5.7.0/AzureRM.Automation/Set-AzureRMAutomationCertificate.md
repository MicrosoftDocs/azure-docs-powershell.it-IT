---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F1A2861F-14EF-4F67-8452-31FD498528BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCertificate.md
ms.openlocfilehash: a1858419b20bf85a40f94e2b5016b461cd24c39a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519941"
---
# <span data-ttu-id="28c0e-101">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="28c0e-101">Set-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="28c0e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="28c0e-103">Modifica la configurazione di un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="28c0e-103">Modifies the configuration of an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28c0e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28c0e-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path <String>] [-Exportable <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28c0e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28c0e-105">DESCRIPTION</span></span>
<span data-ttu-id="28c0e-106">Il cmdlet **set-AzureRmAutomationCertificate** modifica la configurazione di un certificato in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="28c0e-106">The **Set-AzureRmAutomationCertificate** cmdlet modifies the configuration of a certificate in Azure Automation.</span></span>

## <span data-ttu-id="28c0e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28c0e-107">EXAMPLES</span></span>

### <span data-ttu-id="28c0e-108">Esempio 1: modificare un certificato</span><span class="sxs-lookup"><span data-stu-id="28c0e-108">Example 1: Modify a certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> Set-AzureAutomationCertificate -AutomationAccountName "Contos17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="28c0e-109">Il primo comando converte una password di testo normale in una stringa sicura usando il cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="28c0e-109">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="28c0e-110">Il comando Archivia l'oggetto nella variabile $Password.</span><span class="sxs-lookup"><span data-stu-id="28c0e-110">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="28c0e-111">Il secondo comando modifica un certificato denominato ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="28c0e-111">The second command modifies a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="28c0e-112">Il comando usa la password archiviata in $Password.</span><span class="sxs-lookup"><span data-stu-id="28c0e-112">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="28c0e-113">Il comando specifica il nome dell'account e il percorso del file che viene caricato.</span><span class="sxs-lookup"><span data-stu-id="28c0e-113">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="28c0e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28c0e-114">PARAMETERS</span></span>

### <span data-ttu-id="28c0e-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="28c0e-115">-AutomationAccountName</span></span>
<span data-ttu-id="28c0e-116">Specifica il nome dell'account di automazione per cui questo cmdlet modifica un certificato.</span><span class="sxs-lookup"><span data-stu-id="28c0e-116">Specifies the name of the Automation account for which this cmdlet modifies a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28c0e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c0e-117">-DefaultProfile</span></span>
<span data-ttu-id="28c0e-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="28c0e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c0e-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="28c0e-119">-Description</span></span>
<span data-ttu-id="28c0e-120">Specifica una descrizione per il certificato modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28c0e-120">Specifies a description for the certificate that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="28c0e-121">-Esportabile</span><span class="sxs-lookup"><span data-stu-id="28c0e-121">-Exportable</span></span>
<span data-ttu-id="28c0e-122">Specifica se il certificato può essere esportato.</span><span class="sxs-lookup"><span data-stu-id="28c0e-122">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="28c0e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="28c0e-123">-Name</span></span>
<span data-ttu-id="28c0e-124">Specifica il nome del certificato modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28c0e-124">Specifies the name of the certificate that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28c0e-125">-Password</span><span class="sxs-lookup"><span data-stu-id="28c0e-125">-Password</span></span>
<span data-ttu-id="28c0e-126">Specifica la password per il file di certificato.</span><span class="sxs-lookup"><span data-stu-id="28c0e-126">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="28c0e-127">-Path</span><span class="sxs-lookup"><span data-stu-id="28c0e-127">-Path</span></span>
<span data-ttu-id="28c0e-128">Specifica il percorso di un file di script da caricare.</span><span class="sxs-lookup"><span data-stu-id="28c0e-128">Specifies the path to a script file to upload.</span></span>
<span data-ttu-id="28c0e-129">Il file può essere un file con estensione cer o un file PFX.</span><span class="sxs-lookup"><span data-stu-id="28c0e-129">The file can be a .cer file or a .pfx file.</span></span>

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

### <span data-ttu-id="28c0e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28c0e-130">-ResourceGroupName</span></span>
<span data-ttu-id="28c0e-131">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un certificato.</span><span class="sxs-lookup"><span data-stu-id="28c0e-131">Specifies the name of the resource group for which this cmdlet modifies a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28c0e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c0e-132">CommonParameters</span></span>
<span data-ttu-id="28c0e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28c0e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c0e-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28c0e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c0e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28c0e-135">INPUTS</span></span>

### <span data-ttu-id="28c0e-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="28c0e-136">None</span></span>
<span data-ttu-id="28c0e-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="28c0e-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="28c0e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28c0e-138">OUTPUTS</span></span>

### <span data-ttu-id="28c0e-139">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="28c0e-139">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="28c0e-140">Note</span><span class="sxs-lookup"><span data-stu-id="28c0e-140">NOTES</span></span>

## <span data-ttu-id="28c0e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28c0e-141">RELATED LINKS</span></span>

[<span data-ttu-id="28c0e-142">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="28c0e-142">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="28c0e-143">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="28c0e-143">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="28c0e-144">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="28c0e-144">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)


