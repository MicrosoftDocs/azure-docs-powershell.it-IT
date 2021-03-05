---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 8b1da3fda8c8c016dd9cbe039015553f9073a4b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008813"
---
# <span data-ttu-id="dbe30-101">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="dbe30-101">New-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="dbe30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbe30-102">SYNOPSIS</span></span>
<span data-ttu-id="dbe30-103">Crea un certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbe30-103">Creates an integration account certificate.</span></span>

## <span data-ttu-id="dbe30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbe30-104">SYNTAX</span></span>

### <span data-ttu-id="dbe30-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="dbe30-105">PrivateKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbe30-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="dbe30-106">PublicKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbe30-107">Entrambi</span><span class="sxs-lookup"><span data-stu-id="dbe30-107">Both</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbe30-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dbe30-108">DESCRIPTION</span></span>
<span data-ttu-id="dbe30-109">Il cmdlet **New-AzIntegrationAccountCertificate** crea un certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbe30-109">The **New-AzIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="dbe30-110">Questo cmdlet restituisce un oggetto che rappresenta il certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbe30-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="dbe30-111">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse, il nome del certificato, il nome della chiave, la versione della chiave e l'ID vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="dbe30-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="dbe30-112">I valori del file di parametri del modello specificati nella riga di comando hanno la precedenza sui valori dei parametri modello in un oggetto parametro modello.</span><span class="sxs-lookup"><span data-stu-id="dbe30-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="dbe30-113">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="dbe30-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="dbe30-114">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="dbe30-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="dbe30-115">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="dbe30-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dbe30-116">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="dbe30-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dbe30-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbe30-117">EXAMPLES</span></span>

### <span data-ttu-id="dbe30-118">Esempio 1: Creare un certificato di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="dbe30-118">Example 1: Create an integration account certificate</span></span>
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

<span data-ttu-id="dbe30-119">Questo comando crea il certificato dell'account di integrazione nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="dbe30-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="dbe30-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbe30-120">PARAMETERS</span></span>

### <span data-ttu-id="dbe30-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="dbe30-121">-CertificateName</span></span>
<span data-ttu-id="dbe30-122">Specifica un nome per il certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbe30-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="dbe30-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbe30-123">-DefaultProfile</span></span>
<span data-ttu-id="dbe30-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="dbe30-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbe30-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="dbe30-125">-KeyName</span></span>
<span data-ttu-id="dbe30-126">Specifica il nome della chiave del certificato nel vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="dbe30-126">Specifies the name of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="dbe30-127">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="dbe30-127">-KeyVaultId</span></span>
<span data-ttu-id="dbe30-128">Specifica un ID vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="dbe30-128">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="dbe30-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="dbe30-129">-KeyVersion</span></span>
<span data-ttu-id="dbe30-130">Specifica la versione della chiave del certificato nel vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="dbe30-130">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="dbe30-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="dbe30-131">-Metadata</span></span>
<span data-ttu-id="dbe30-132">Specifica un oggetto metadati per il certificato.</span><span class="sxs-lookup"><span data-stu-id="dbe30-132">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="dbe30-133">-Name</span><span class="sxs-lookup"><span data-stu-id="dbe30-133">-Name</span></span>
<span data-ttu-id="dbe30-134">Specifica il nome di un account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="dbe30-134">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="dbe30-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="dbe30-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="dbe30-136">Specifica il percorso di un file di certificato pubblico (con estensione cer).</span><span class="sxs-lookup"><span data-stu-id="dbe30-136">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="dbe30-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbe30-137">-ResourceGroupName</span></span>
<span data-ttu-id="dbe30-138">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dbe30-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dbe30-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbe30-139">-Confirm</span></span>
<span data-ttu-id="dbe30-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbe30-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbe30-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbe30-141">-WhatIf</span></span>
<span data-ttu-id="dbe30-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbe30-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbe30-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbe30-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbe30-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbe30-144">CommonParameters</span></span>
<span data-ttu-id="dbe30-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbe30-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbe30-146">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbe30-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbe30-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="dbe30-147">INPUTS</span></span>

### <span data-ttu-id="dbe30-148">System.String</span><span class="sxs-lookup"><span data-stu-id="dbe30-148">System.String</span></span>

## <span data-ttu-id="dbe30-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbe30-149">OUTPUTS</span></span>

### <span data-ttu-id="dbe30-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="dbe30-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="dbe30-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="dbe30-151">NOTES</span></span>

## <span data-ttu-id="dbe30-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbe30-152">RELATED LINKS</span></span>

[<span data-ttu-id="dbe30-153">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="dbe30-153">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="dbe30-154">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="dbe30-154">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="dbe30-155">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="dbe30-155">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


