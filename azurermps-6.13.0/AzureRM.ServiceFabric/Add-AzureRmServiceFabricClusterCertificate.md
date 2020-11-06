---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: fa357a4f5b8e599858ce5aff3e0aa11121833ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516455"
---
# <span data-ttu-id="6b929-101">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6b929-101">Add-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="6b929-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b929-102">SYNOPSIS</span></span>
<span data-ttu-id="6b929-103">Aggiungere un certificato di cluster secondario al cluster.</span><span class="sxs-lookup"><span data-stu-id="6b929-103">Add a secondary cluster certificate to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b929-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b929-104">SYNTAX</span></span>

### <span data-ttu-id="6b929-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="6b929-105">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b929-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="6b929-106">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b929-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="6b929-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b929-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b929-108">DESCRIPTION</span></span>
<span data-ttu-id="6b929-109">Usare **Add-AzureRmServiceFabricClusterCertificate** per aggiungere un certificato di cluster secondario, da un Vault di una chiave di Azure esistente o creare un nuovo Vault di chiave di Azure usando un certificato esistente fornito o da un nuovo certificato autofirmato creato.</span><span class="sxs-lookup"><span data-stu-id="6b929-109">Use **Add-AzureRmServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="6b929-110">Verrà eseguito l'override del cluster secondario, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="6b929-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="6b929-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b929-111">EXAMPLES</span></span>

### <span data-ttu-id="6b929-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6b929-112">Example 1</span></span>
```
Add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="6b929-113">Questo comando aggiungerà un certificato nell'archivio di chiavi di Azure esistente come certificato di cluster secondario.</span><span class="sxs-lookup"><span data-stu-id="6b929-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="6b929-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="6b929-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="6b929-115">Questo comando creerà un certificato autofirmato nel Vault di Azure Key e aggiornerà il cluster per usarlo come certificato di cluster secondario.</span><span class="sxs-lookup"><span data-stu-id="6b929-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="6b929-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b929-116">PARAMETERS</span></span>

### <span data-ttu-id="6b929-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="6b929-117">-CertificateFile</span></span>
<span data-ttu-id="6b929-118">Percorso del file del certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="6b929-118">The existing certificate file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b929-119">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="6b929-119">-CertificateOutputFolder</span></span>
<span data-ttu-id="6b929-120">Cartella del nuovo certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="6b929-120">The folder of the new certificate to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b929-121">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="6b929-121">-CertificatePassword</span></span>
<span data-ttu-id="6b929-122">La password del file di certificato.</span><span class="sxs-lookup"><span data-stu-id="6b929-122">The password of the certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b929-123">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="6b929-123">-CertificateSubjectName</span></span>
<span data-ttu-id="6b929-124">Nome DNS del certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="6b929-124">The Dns name of the certificate to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName
Aliases: Subject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b929-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b929-125">-DefaultProfile</span></span>
<span data-ttu-id="6b929-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b929-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b929-127">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="6b929-127">-KeyVaultName</span></span>
<span data-ttu-id="6b929-128">Nome del Vault della chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="6b929-128">Azure key vault name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b929-129">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b929-129">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="6b929-130">Nome del gruppo di risorse di Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="6b929-130">Azure key vault resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b929-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b929-131">-Name</span></span>
<span data-ttu-id="6b929-132">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="6b929-132">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b929-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b929-133">-ResourceGroupName</span></span>
<span data-ttu-id="6b929-134">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6b929-134">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6b929-135">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="6b929-135">-SecretIdentifier</span></span>
<span data-ttu-id="6b929-136">URL segreto del Vault Key di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="6b929-136">The existing Azure key vault secret Url.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b929-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b929-137">-Confirm</span></span>
<span data-ttu-id="6b929-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b929-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b929-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b929-139">-WhatIf</span></span>
<span data-ttu-id="6b929-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b929-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6b929-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b929-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b929-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b929-142">CommonParameters</span></span>
<span data-ttu-id="6b929-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b929-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b929-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b929-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b929-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b929-145">INPUTS</span></span>

### <span data-ttu-id="6b929-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6b929-146">System.String</span></span>
<span data-ttu-id="6b929-147">Parametri: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), VAULTNAME (ByValue), KeyVaultResouceGroupName (ByValue), SecretIdentifier (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b929-147">Parameters: CertificateFile (ByValue), CertificateOutputFolder (ByValue), CertificateSubjectName (ByValue), KeyVaultName (ByValue), KeyVaultResouceGroupName (ByValue), SecretIdentifier (ByValue)</span></span>

### <span data-ttu-id="6b929-148">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="6b929-148">System.Security.SecureString</span></span>
<span data-ttu-id="6b929-149">Parametri: CertificatePassword (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b929-149">Parameters: CertificatePassword (ByValue)</span></span>

## <span data-ttu-id="6b929-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b929-150">OUTPUTS</span></span>

### <span data-ttu-id="6b929-151">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="6b929-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="6b929-152">Note</span><span class="sxs-lookup"><span data-stu-id="6b929-152">NOTES</span></span>

## <span data-ttu-id="6b929-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b929-153">RELATED LINKS</span></span>

[<span data-ttu-id="6b929-154">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="6b929-154">Remove-AzureRmServiceFabricClusterCertificate</span></span>](./Remove-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="6b929-155">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6b929-155">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)

[<span data-ttu-id="6b929-156">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="6b929-156">Add-AzureRmServiceFabricApplicationCertificate</span></span>](./Add-AzureRmServiceFabricApplicationCertificate.md)
