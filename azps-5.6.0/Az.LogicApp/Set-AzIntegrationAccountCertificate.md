---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
ms.openlocfilehash: c7ae1404cfff2d725326b9f5a8f2b7244c030109
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996644"
---
# <span data-ttu-id="819ed-101">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="819ed-101">Set-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="819ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="819ed-102">SYNOPSIS</span></span>
<span data-ttu-id="819ed-103">Modifica un certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="819ed-103">Modifies an integration account certificate.</span></span>

## <span data-ttu-id="819ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="819ed-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="819ed-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="819ed-105">DESCRIPTION</span></span>
<span data-ttu-id="819ed-106">Il **cmdlet Set-AzIntegrationAccountCertificate** modifica un certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="819ed-106">The **Set-AzIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="819ed-107">Questo cmdlet restituisce un oggetto che rappresenta il certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="819ed-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="819ed-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="819ed-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="819ed-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="819ed-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="819ed-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="819ed-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="819ed-111">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="819ed-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="819ed-112">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="819ed-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="819ed-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="819ed-113">EXAMPLES</span></span>

### <span data-ttu-id="819ed-114">Esempio 1: Modificare un certificato di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="819ed-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="819ed-115">Questo comando modifica il certificato dell'account di integrazione nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="819ed-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="819ed-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="819ed-116">PARAMETERS</span></span>

### <span data-ttu-id="819ed-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="819ed-117">-CertificateName</span></span>
<span data-ttu-id="819ed-118">Specifica il nome di un certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="819ed-118">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819ed-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="819ed-119">-DefaultProfile</span></span>
<span data-ttu-id="819ed-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="819ed-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="819ed-121">-Force</span><span class="sxs-lookup"><span data-stu-id="819ed-121">-Force</span></span>
<span data-ttu-id="819ed-122">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="819ed-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819ed-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="819ed-123">-KeyName</span></span>
<span data-ttu-id="819ed-124">Specifica il nome di una chiave del certificato nel vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="819ed-124">Specifies the name of a certificate key in the key vault.</span></span>

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

### <span data-ttu-id="819ed-125">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="819ed-125">-KeyVaultId</span></span>
<span data-ttu-id="819ed-126">Specifica un ID vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="819ed-126">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="819ed-127">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="819ed-127">-KeyVersion</span></span>
<span data-ttu-id="819ed-128">Specifica la versione della chiave del certificato nel vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="819ed-128">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="819ed-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="819ed-129">-Metadata</span></span>
<span data-ttu-id="819ed-130">Specifica un oggetto metadati per il certificato.</span><span class="sxs-lookup"><span data-stu-id="819ed-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="819ed-131">-Name</span><span class="sxs-lookup"><span data-stu-id="819ed-131">-Name</span></span>
<span data-ttu-id="819ed-132">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="819ed-132">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819ed-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="819ed-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="819ed-134">Specifica il percorso di un file di certificato pubblico (con estensione cer).</span><span class="sxs-lookup"><span data-stu-id="819ed-134">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="819ed-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="819ed-135">-ResourceGroupName</span></span>
<span data-ttu-id="819ed-136">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="819ed-136">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819ed-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="819ed-137">-Confirm</span></span>
<span data-ttu-id="819ed-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="819ed-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="819ed-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="819ed-139">-WhatIf</span></span>
<span data-ttu-id="819ed-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="819ed-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="819ed-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="819ed-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="819ed-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="819ed-142">CommonParameters</span></span>
<span data-ttu-id="819ed-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="819ed-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="819ed-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="819ed-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="819ed-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="819ed-145">INPUTS</span></span>

### <span data-ttu-id="819ed-146">System.String</span><span class="sxs-lookup"><span data-stu-id="819ed-146">System.String</span></span>

## <span data-ttu-id="819ed-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="819ed-147">OUTPUTS</span></span>

### <span data-ttu-id="819ed-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="819ed-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="819ed-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="819ed-149">NOTES</span></span>

## <span data-ttu-id="819ed-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="819ed-150">RELATED LINKS</span></span>

[<span data-ttu-id="819ed-151">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="819ed-151">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="819ed-152">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="819ed-152">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="819ed-153">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="819ed-153">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)


