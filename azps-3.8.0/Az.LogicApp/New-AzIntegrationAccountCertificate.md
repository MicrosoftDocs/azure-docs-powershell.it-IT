---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 651ce1141e9a925d5571f8b70d8eecedb4a1e66d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019831"
---
# <span data-ttu-id="ad1b1-101">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ad1b1-101">New-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="ad1b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ad1b1-102">SYNOPSIS</span></span>
<span data-ttu-id="ad1b1-103">Crea un certificato per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-103">Creates an integration account certificate.</span></span>

## <span data-ttu-id="ad1b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad1b1-104">SYNTAX</span></span>

### <span data-ttu-id="ad1b1-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="ad1b1-105">PrivateKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad1b1-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="ad1b1-106">PublicKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad1b1-107">Sia</span><span class="sxs-lookup"><span data-stu-id="ad1b1-107">Both</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad1b1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad1b1-108">DESCRIPTION</span></span>
<span data-ttu-id="ad1b1-109">Il cmdlet **New-AzIntegrationAccountCertificate** crea un certificato per l'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-109">The **New-AzIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="ad1b1-110">Questo cmdlet restituisce un oggetto che rappresenta il certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="ad1b1-111">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse, il nome del certificato, il nome della chiave, la versione chiave e l'ID chiave.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="ad1b1-112">I valori dei parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri del modello in un oggetto parametro di modello.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="ad1b1-113">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ad1b1-114">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ad1b1-115">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ad1b1-116">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ad1b1-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad1b1-117">EXAMPLES</span></span>

### <span data-ttu-id="ad1b1-118">Esempio 1: creare un certificato per l'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ad1b1-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="ad1b1-119">Questo comando crea il certificato dell'account di integrazione nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="ad1b1-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ad1b1-120">PARAMETERS</span></span>

### <span data-ttu-id="ad1b1-121">-Certificate</span><span class="sxs-lookup"><span data-stu-id="ad1b1-121">-CertificateName</span></span>
<span data-ttu-id="ad1b1-122">Specifica un nome per il certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-122">Specifies a name for the integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1b1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad1b1-123">-DefaultProfile</span></span>
<span data-ttu-id="ad1b1-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ad1b1-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad1b1-125">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="ad1b1-125">-KeyName</span></span>
<span data-ttu-id="ad1b1-126">Specifica il nome della chiave del certificato nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-126">Specifies the name of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1b1-127">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="ad1b1-127">-KeyVaultId</span></span>
<span data-ttu-id="ad1b1-128">Specifica un ID di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-128">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1b1-129">-Versione</span><span class="sxs-lookup"><span data-stu-id="ad1b1-129">-KeyVersion</span></span>
<span data-ttu-id="ad1b1-130">Specifica la versione della chiave del certificato nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-130">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1b1-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ad1b1-131">-Metadata</span></span>
<span data-ttu-id="ad1b1-132">Specifica un oggetto Metadata per il certificato.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-132">Specifies a metadata object for the certificate.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1b1-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="ad1b1-133">-Name</span></span>
<span data-ttu-id="ad1b1-134">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-134">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1b1-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="ad1b1-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="ad1b1-136">Specifica il percorso di un file di certificato pubblico (con estensione CER).</span><span class="sxs-lookup"><span data-stu-id="ad1b1-136">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1b1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad1b1-137">-ResourceGroupName</span></span>
<span data-ttu-id="ad1b1-138">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-138">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1b1-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ad1b1-139">-Confirm</span></span>
<span data-ttu-id="ad1b1-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1b1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad1b1-141">-WhatIf</span></span>
<span data-ttu-id="ad1b1-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad1b1-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad1b1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad1b1-144">CommonParameters</span></span>
<span data-ttu-id="ad1b1-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad1b1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad1b1-146">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad1b1-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad1b1-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ad1b1-147">INPUTS</span></span>

### <span data-ttu-id="ad1b1-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ad1b1-148">System.String</span></span>

## <span data-ttu-id="ad1b1-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad1b1-149">OUTPUTS</span></span>

### <span data-ttu-id="ad1b1-150">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ad1b1-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="ad1b1-151">Note</span><span class="sxs-lookup"><span data-stu-id="ad1b1-151">NOTES</span></span>

## <span data-ttu-id="ad1b1-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad1b1-152">RELATED LINKS</span></span>

[<span data-ttu-id="ad1b1-153">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ad1b1-153">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="ad1b1-154">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ad1b1-154">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="ad1b1-155">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ad1b1-155">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


