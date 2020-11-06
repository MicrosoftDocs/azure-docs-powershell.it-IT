---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: 498b09867436e6aa272abd8796b41f159cd388f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520755"
---
# <span data-ttu-id="4b88a-101">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="4b88a-101">Add-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="4b88a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b88a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b88a-103">Aggiungere un certificato di cluster secondario al cluster.</span><span class="sxs-lookup"><span data-stu-id="4b88a-103">Add a secondary cluster certificate to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b88a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b88a-104">SYNTAX</span></span>

### <span data-ttu-id="4b88a-105">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="4b88a-105">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b88a-106">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="4b88a-106">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b88a-107">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="4b88a-107">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricClusterCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b88a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b88a-108">DESCRIPTION</span></span>
<span data-ttu-id="4b88a-109">Usare **Add-AzureRmServiceFabricClusterCertificate** per aggiungere un certificato di cluster secondario, da un Vault di una chiave di Azure esistente o creare un nuovo Vault di chiave di Azure usando un certificato esistente fornito o da un nuovo certificato autofirmato creato.</span><span class="sxs-lookup"><span data-stu-id="4b88a-109">Use **Add-AzureRmServiceFabricClusterCertificate** to add a secondary cluster certificate, either from an existing Azure key vault or creating a new Azure key vault using an existing certificate provided or from a new self-signed certificate created.</span></span> <span data-ttu-id="4b88a-110">Verrà eseguito l'override del cluster secondario, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="4b88a-110">It will override the secondary cluster if there is any.</span></span>

## <span data-ttu-id="4b88a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b88a-111">EXAMPLES</span></span>

### <span data-ttu-id="4b88a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4b88a-112">Example 1</span></span>
```
Add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' 
-SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="4b88a-113">Questo comando aggiungerà un certificato nell'archivio di chiavi di Azure esistente come certificato di cluster secondario.</span><span class="sxs-lookup"><span data-stu-id="4b88a-113">This command will add a certificate in the existing Azure key vault as a secondary cluster certificate.</span></span>

### <span data-ttu-id="4b88a-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4b88a-114">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String "123" -AsPlainText -Force
PS c:\> add-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster'  -CertificateSubjectName 'Contoso.com' 
-CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="4b88a-115">Questo comando creerà un certificato autofirmato nel Vault di Azure Key e aggiornerà il cluster per usarlo come certificato di cluster secondario.</span><span class="sxs-lookup"><span data-stu-id="4b88a-115">This command will create a self-signed certificate in the Azure key vault and upgrade the cluster to use it as a secondary cluster certificate.</span></span>

## <span data-ttu-id="4b88a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b88a-116">PARAMETERS</span></span>

### <span data-ttu-id="4b88a-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="4b88a-117">-CertificateFile</span></span>
<span data-ttu-id="4b88a-118">Percorso del file del certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="4b88a-118">The existing certificate file path.</span></span>

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

### <span data-ttu-id="4b88a-119">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="4b88a-119">-CertificateOutputFolder</span></span>
<span data-ttu-id="4b88a-120">Cartella del nuovo certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="4b88a-120">The folder of the new certificate to be created.</span></span>

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

### <span data-ttu-id="4b88a-121">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="4b88a-121">-CertificatePassword</span></span>
<span data-ttu-id="4b88a-122">La password del file di certificato.</span><span class="sxs-lookup"><span data-stu-id="4b88a-122">The password of the certificate file.</span></span>

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

### <span data-ttu-id="4b88a-123">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="4b88a-123">-CertificateSubjectName</span></span>
<span data-ttu-id="4b88a-124">Nome DNS del certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="4b88a-124">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="4b88a-125">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="4b88a-125">-KeyVaultName</span></span>
<span data-ttu-id="4b88a-126">Nome del Vault della chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b88a-126">Azure key vault name.</span></span>

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

### <span data-ttu-id="4b88a-127">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b88a-127">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="4b88a-128">Nome del gruppo di risorse di Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="4b88a-128">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="4b88a-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b88a-129">-Name</span></span>
<span data-ttu-id="4b88a-130">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="4b88a-130">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4b88a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b88a-131">-ResourceGroupName</span></span>
<span data-ttu-id="4b88a-132">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b88a-132">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4b88a-133">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="4b88a-133">-SecretIdentifier</span></span>
<span data-ttu-id="4b88a-134">URL segreto del Vault Key di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="4b88a-134">The existing Azure key vault secret Url.</span></span>

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

### <span data-ttu-id="4b88a-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4b88a-135">-Confirm</span></span>
<span data-ttu-id="4b88a-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b88a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b88a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b88a-137">-WhatIf</span></span>
<span data-ttu-id="4b88a-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b88a-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b88a-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b88a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b88a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b88a-140">-DefaultProfile</span></span>
<span data-ttu-id="4b88a-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b88a-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b88a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b88a-142">CommonParameters</span></span>
<span data-ttu-id="4b88a-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b88a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b88a-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b88a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b88a-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b88a-145">INPUTS</span></span>

### <span data-ttu-id="4b88a-146">System. String</span><span class="sxs-lookup"><span data-stu-id="4b88a-146">System.String</span></span>

## <span data-ttu-id="4b88a-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b88a-147">OUTPUTS</span></span>

### <span data-ttu-id="4b88a-148">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="4b88a-148">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="4b88a-149">Note</span><span class="sxs-lookup"><span data-stu-id="4b88a-149">NOTES</span></span>

## <span data-ttu-id="4b88a-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b88a-150">RELATED LINKS</span></span>

[<span data-ttu-id="4b88a-151">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="4b88a-151">Remove-AzureRmServiceFabricClusterCertificate</span></span>](./Remove-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="4b88a-152">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="4b88a-152">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)

[<span data-ttu-id="4b88a-153">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="4b88a-153">Add-AzureRmServiceFabricApplicationCertificate</span></span>](./Add-AzureRmServiceFabricApplicationCertificate.md)
