---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: feb885ca6f08a7396fd88db73d48172dc002f055
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520055"
---
# <span data-ttu-id="1f94a-101">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1f94a-101">Set-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="1f94a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f94a-102">SYNOPSIS</span></span>
<span data-ttu-id="1f94a-103">Modifica un certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1f94a-103">Modifies an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f94a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f94a-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f94a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f94a-105">DESCRIPTION</span></span>
<span data-ttu-id="1f94a-106">Il cmdlet **set-AzureRmIntegrationAccountCertificate** modifica un certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1f94a-106">The **Set-AzureRmIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="1f94a-107">Questo cmdlet restituisce un oggetto che rappresenta il certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1f94a-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="1f94a-108">Specificare il nome dell'account di integrazione, il nome del gruppo di risorse e il nome del certificato.</span><span class="sxs-lookup"><span data-stu-id="1f94a-108">Specifying the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="1f94a-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="1f94a-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1f94a-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="1f94a-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1f94a-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="1f94a-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1f94a-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="1f94a-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1f94a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f94a-113">EXAMPLES</span></span>

### <span data-ttu-id="1f94a-114">Esempio 1: modificare un certificato dell'account di integrazione</span><span class="sxs-lookup"><span data-stu-id="1f94a-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegartionAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="1f94a-115">Questo comando modifica il certificato dell'account di integrazione nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="1f94a-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="1f94a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f94a-116">PARAMETERS</span></span>

### <span data-ttu-id="1f94a-117">-Certificate</span><span class="sxs-lookup"><span data-stu-id="1f94a-117">-CertificateName</span></span>
<span data-ttu-id="1f94a-118">Specifica il nome di un certificato dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1f94a-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="1f94a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1f94a-119">-Force</span></span>
<span data-ttu-id="1f94a-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1f94a-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1f94a-121">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="1f94a-121">-KeyName</span></span>
<span data-ttu-id="1f94a-122">Specifica il nome di una chiave di certificato nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="1f94a-122">Specifies the name of a certificate key in the key vault.</span></span>

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

### <span data-ttu-id="1f94a-123">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="1f94a-123">-KeyVaultId</span></span>
<span data-ttu-id="1f94a-124">Specifica un ID di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="1f94a-124">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="1f94a-125">-Versione</span><span class="sxs-lookup"><span data-stu-id="1f94a-125">-KeyVersion</span></span>
<span data-ttu-id="1f94a-126">Specifica la versione della chiave del certificato nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="1f94a-126">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="1f94a-127">-Metadata</span><span class="sxs-lookup"><span data-stu-id="1f94a-127">-Metadata</span></span>
<span data-ttu-id="1f94a-128">Specifica un oggetto Metadata per il certificato.</span><span class="sxs-lookup"><span data-stu-id="1f94a-128">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="1f94a-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f94a-129">-Name</span></span>
<span data-ttu-id="1f94a-130">Specifica il nome dell'account di integrazione.</span><span class="sxs-lookup"><span data-stu-id="1f94a-130">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="1f94a-131">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="1f94a-131">-PublicCertificateFilePath</span></span>
<span data-ttu-id="1f94a-132">Specifica il percorso di un file di certificato pubblico (con estensione CER).</span><span class="sxs-lookup"><span data-stu-id="1f94a-132">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="1f94a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f94a-133">-ResourceGroupName</span></span>
<span data-ttu-id="1f94a-134">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1f94a-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1f94a-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f94a-135">-Confirm</span></span>
<span data-ttu-id="1f94a-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f94a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f94a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f94a-137">-WhatIf</span></span>
<span data-ttu-id="1f94a-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f94a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f94a-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f94a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f94a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f94a-140">-DefaultProfile</span></span>
<span data-ttu-id="1f94a-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f94a-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f94a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f94a-142">CommonParameters</span></span>
<span data-ttu-id="1f94a-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f94a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f94a-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f94a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f94a-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f94a-145">INPUTS</span></span>

## <span data-ttu-id="1f94a-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f94a-146">OUTPUTS</span></span>

### <span data-ttu-id="1f94a-147">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1f94a-147">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="1f94a-148">Note</span><span class="sxs-lookup"><span data-stu-id="1f94a-148">NOTES</span></span>

## <span data-ttu-id="1f94a-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f94a-149">RELATED LINKS</span></span>

[<span data-ttu-id="1f94a-150">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1f94a-150">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="1f94a-151">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1f94a-151">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="1f94a-152">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1f94a-152">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

