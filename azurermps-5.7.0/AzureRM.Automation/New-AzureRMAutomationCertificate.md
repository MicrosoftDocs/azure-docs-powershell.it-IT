---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCertificate.md
ms.openlocfilehash: e82d78254e81a5b8fb98c1dfbfac2113d19361a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508403"
---
# <span data-ttu-id="3a245-101">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3a245-101">New-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="3a245-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3a245-102">SYNOPSIS</span></span>
<span data-ttu-id="3a245-103">Crea un certificato di automazione.</span><span class="sxs-lookup"><span data-stu-id="3a245-103">Creates an Automation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a245-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a245-104">SYNTAX</span></span>

```
New-AzureRmAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a245-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a245-105">DESCRIPTION</span></span>
<span data-ttu-id="3a245-106">Il cmdlet **New-AzureRmAutomationCertificate** crea un certificato in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3a245-106">The **New-AzureRmAutomationCertificate** cmdlet creates a certificate in Azure Automation.</span></span>
<span data-ttu-id="3a245-107">Specificare il percorso di un file di certificato da caricare.</span><span class="sxs-lookup"><span data-stu-id="3a245-107">Provide the path to a certificate file to upload.</span></span>

## <span data-ttu-id="3a245-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a245-108">EXAMPLES</span></span>

### <span data-ttu-id="3a245-109">Esempio 1: creare un nuovo certificato</span><span class="sxs-lookup"><span data-stu-id="3a245-109">Example 1: Create a new certificate</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzureRmAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3a245-110">Il primo comando converte una password di testo normale in una stringa sicura usando il cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="3a245-110">The first command converts a plain text password to be a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="3a245-111">Il comando Archivia l'oggetto nella variabile $Password.</span><span class="sxs-lookup"><span data-stu-id="3a245-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="3a245-112">Il secondo comando crea un certificato denominato ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="3a245-112">The second command creates a certificate named ContosoCertificate.</span></span>
<span data-ttu-id="3a245-113">Il comando usa la password archiviata in $Password.</span><span class="sxs-lookup"><span data-stu-id="3a245-113">The command uses the password stored in $Password.</span></span>
<span data-ttu-id="3a245-114">Il comando specifica il nome dell'account e il percorso del file che viene caricato.</span><span class="sxs-lookup"><span data-stu-id="3a245-114">The command specifies the account name and the path of the file that it uploads.</span></span>

## <span data-ttu-id="3a245-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3a245-115">PARAMETERS</span></span>

### <span data-ttu-id="3a245-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3a245-116">-AutomationAccountName</span></span>
<span data-ttu-id="3a245-117">Specifica il nome dell'account di automazione per il quale questo cmdlet archivia il certificato.</span><span class="sxs-lookup"><span data-stu-id="3a245-117">Specifies the name of the Automation account for which this cmdlet stores the certificate.</span></span>

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

### <span data-ttu-id="3a245-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a245-118">-DefaultProfile</span></span>
<span data-ttu-id="3a245-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3a245-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a245-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a245-120">-Description</span></span>
<span data-ttu-id="3a245-121">Specifica una descrizione per il certificato.</span><span class="sxs-lookup"><span data-stu-id="3a245-121">Specifies a description for the certificate.</span></span>

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

### <span data-ttu-id="3a245-122">-Esportabile</span><span class="sxs-lookup"><span data-stu-id="3a245-122">-Exportable</span></span>
<span data-ttu-id="3a245-123">Specifica se il certificato può essere esportato.</span><span class="sxs-lookup"><span data-stu-id="3a245-123">Specifies whether the certificate can be exported.</span></span>

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

### <span data-ttu-id="3a245-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="3a245-124">-Name</span></span>
<span data-ttu-id="3a245-125">Specifica il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="3a245-125">Specifies the name for the certificate.</span></span>

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

### <span data-ttu-id="3a245-126">-Password</span><span class="sxs-lookup"><span data-stu-id="3a245-126">-Password</span></span>
<span data-ttu-id="3a245-127">Specifica la password per il file di certificato.</span><span class="sxs-lookup"><span data-stu-id="3a245-127">Specifies the password for the certificate file.</span></span>

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

### <span data-ttu-id="3a245-128">-Path</span><span class="sxs-lookup"><span data-stu-id="3a245-128">-Path</span></span>
<span data-ttu-id="3a245-129">Specifica il percorso di un file di script caricato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a245-129">Specifies the path to a script file that this cmdlet uploads.</span></span>
<span data-ttu-id="3a245-130">Il file può essere un file con estensione cer o PFX.</span><span class="sxs-lookup"><span data-stu-id="3a245-130">The file can be a .cer or a .pfx file.</span></span>

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

### <span data-ttu-id="3a245-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a245-131">-ResourceGroupName</span></span>
<span data-ttu-id="3a245-132">Specifica il nome del gruppo di risorse per cui questo cmdlet crea un certificato.</span><span class="sxs-lookup"><span data-stu-id="3a245-132">Specifies the name of the resource group for which this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="3a245-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a245-133">CommonParameters</span></span>
<span data-ttu-id="3a245-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a245-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a245-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a245-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a245-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3a245-136">INPUTS</span></span>

### <span data-ttu-id="3a245-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3a245-137">None</span></span>
<span data-ttu-id="3a245-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="3a245-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a245-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a245-139">OUTPUTS</span></span>

### <span data-ttu-id="3a245-140">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="3a245-140">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="3a245-141">Note</span><span class="sxs-lookup"><span data-stu-id="3a245-141">NOTES</span></span>

## <span data-ttu-id="3a245-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a245-142">RELATED LINKS</span></span>

[<span data-ttu-id="3a245-143">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3a245-143">Get-AzureRmAutomationCertificate</span></span>](./Get-AzureRMAutomationCertificate.md)

[<span data-ttu-id="3a245-144">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3a245-144">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="3a245-145">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3a245-145">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


