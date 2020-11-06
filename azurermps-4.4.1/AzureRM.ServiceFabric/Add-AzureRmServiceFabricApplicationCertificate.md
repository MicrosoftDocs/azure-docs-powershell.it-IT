---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricApplicationCertificate.md
ms.openlocfilehash: 6d77c795415bca1a8bffbed6d09062f394782e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520756"
---
# <span data-ttu-id="268d3-101">Add-AzureRmServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="268d3-101">Add-AzureRmServiceFabricApplicationCertificate</span></span>

## <span data-ttu-id="268d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="268d3-102">SYNOPSIS</span></span>
<span data-ttu-id="268d3-103">Aggiungere un nuovo certificato ai set di scale della macchina virtuale che compongono il cluster.</span><span class="sxs-lookup"><span data-stu-id="268d3-103">Add a new certificate to the Virtual Machine Scale Set(s) that make up the cluster.</span></span> <span data-ttu-id="268d3-104">Il certificato è destinato a essere usato come certificato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="268d3-104">The certificate is intended to be used as an application certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="268d3-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="268d3-105">SYNTAX</span></span>

### <span data-ttu-id="268d3-106">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="268d3-106">ByExistingKeyVault</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="268d3-107">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="268d3-107">ByNewPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] -CertificateSubjectName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="268d3-108">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="268d3-108">ByExistingPfxAndVaultName</span></span>
```
Add-AzureRmServiceFabricApplicationCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>] -CertificateFile <String>
 [-CertificatePassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="268d3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="268d3-109">DESCRIPTION</span></span>
<span data-ttu-id="268d3-110">Usare **Add-AzureRmServiceFabricApplicationCertificate** per installare un certificato in tutti i nodi del cluster.</span><span class="sxs-lookup"><span data-stu-id="268d3-110">Use **Add-AzureRmServiceFabricApplicationCertificate** to install a certificate to all nodes in the cluster.</span></span> <span data-ttu-id="268d3-111">Puoi specificare un certificato che hai già o avere il sistema per generarne uno nuovo e caricarlo in un Vault di chiave di Azure nuovo o esistente.</span><span class="sxs-lookup"><span data-stu-id="268d3-111">You can specify a certificate you already have or have the system generate a new one for you, and upload it to a new or existing Azure key vault.</span></span>

## <span data-ttu-id="268d3-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="268d3-112">EXAMPLES</span></span>

### <span data-ttu-id="268d3-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="268d3-113">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SecretIdentifier 'https://contoso03vault.vault.azure.net/secrets/contoso03vaultrg/7f7de9131c034172b9df37ccc549524f'
```

<span data-ttu-id="268d3-114">Questo comando aggiungerà un certificato dall'archivio di chiavi di Azure esistente a tutti i tipi di nodo del cluster.</span><span class="sxs-lookup"><span data-stu-id="268d3-114">This command will add a certificate from existing Azure key vault to all node types of the cluster.</span></span>

### <span data-ttu-id="268d3-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="268d3-115">Example 2</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String '123' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricApplicationCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -KeyVaultName 'Contoso02Vault' -KeyVaultResouceGroupName 'Contoso02VaultRg'
        -CertificateSubjectName 'cn=Contoso.com' -CertificateOutputFolder 'c:\test' -CertificatePassword $pwd
```

<span data-ttu-id="268d3-116">Questo comando creerà un certificato autofirmato nel Vault di chiave di Azure con il nome del gruppo di risorse del Vault chiave e il nome della chiave del Vault, viene installato in tutti i tipi di nodo del cluster e Scarica il certificato nella cartella "c:\test".</span><span class="sxs-lookup"><span data-stu-id="268d3-116">This command will create a self-signed certificate in the Azure key vault with the key vault resource group name and key vault Name, installs to all node types of the cluster, and downloads the certificate under folder 'c:\test'.</span></span> <span data-ttu-id="268d3-117">Il nome del certificato scaricato è uguale al nome del certificato di volta chiave.</span><span class="sxs-lookup"><span data-stu-id="268d3-117">The name of the certificate downloaded is same as the name of key vault certificate.</span></span>

## <span data-ttu-id="268d3-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="268d3-118">PARAMETERS</span></span>

### <span data-ttu-id="268d3-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="268d3-119">-CertificateFile</span></span>
<span data-ttu-id="268d3-120">Percorso del file del certificato esistente.</span><span class="sxs-lookup"><span data-stu-id="268d3-120">The existing certificate file path.</span></span>

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

### <span data-ttu-id="268d3-121">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="268d3-121">-CertificateOutputFolder</span></span>
<span data-ttu-id="268d3-122">Percorso cartella del nuovo certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="268d3-122">The folder path of the new certificate to be created.</span></span>

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

### <span data-ttu-id="268d3-123">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="268d3-123">-CertificatePassword</span></span>
<span data-ttu-id="268d3-124">La password del file PFX.</span><span class="sxs-lookup"><span data-stu-id="268d3-124">The password of the pfx file.</span></span>

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

### <span data-ttu-id="268d3-125">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="268d3-125">-CertificateSubjectName</span></span>
<span data-ttu-id="268d3-126">Nome DNS del certificato da creare.</span><span class="sxs-lookup"><span data-stu-id="268d3-126">The Dns name of the certificate to be created.</span></span>

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

### <span data-ttu-id="268d3-127">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="268d3-127">-KeyVaultName</span></span>
<span data-ttu-id="268d3-128">Nome del Vault della chiave di Azure.</span><span class="sxs-lookup"><span data-stu-id="268d3-128">Azure key vault name.</span></span>

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

### <span data-ttu-id="268d3-129">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="268d3-129">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="268d3-130">Nome del gruppo di risorse di Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="268d3-130">Azure key vault resource group name.</span></span>

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

### <span data-ttu-id="268d3-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="268d3-131">-Name</span></span>
<span data-ttu-id="268d3-132">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="268d3-132">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="268d3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="268d3-133">-ResourceGroupName</span></span>
<span data-ttu-id="268d3-134">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="268d3-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="268d3-135">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="268d3-135">-SecretIdentifier</span></span>
<span data-ttu-id="268d3-136">URI segreto del Vault Key di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="268d3-136">The existing Azure key vault secret uri.</span></span>

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

### <span data-ttu-id="268d3-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="268d3-137">-Confirm</span></span>
<span data-ttu-id="268d3-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="268d3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="268d3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="268d3-139">-WhatIf</span></span>
<span data-ttu-id="268d3-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="268d3-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="268d3-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="268d3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="268d3-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268d3-142">-DefaultProfile</span></span>
<span data-ttu-id="268d3-143">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="268d3-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="268d3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268d3-144">CommonParameters</span></span>
<span data-ttu-id="268d3-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="268d3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268d3-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="268d3-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268d3-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="268d3-147">INPUTS</span></span>

### <span data-ttu-id="268d3-148">System. String</span><span class="sxs-lookup"><span data-stu-id="268d3-148">System.String</span></span>

## <span data-ttu-id="268d3-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="268d3-149">OUTPUTS</span></span>

### <span data-ttu-id="268d3-150">Microsoft. Azure. Commands. ServiceFabric. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="268d3-150">Microsoft.Azure.Commands.ServiceFabric.Models.PSKeyVault</span></span>

## <span data-ttu-id="268d3-151">Note</span><span class="sxs-lookup"><span data-stu-id="268d3-151">NOTES</span></span>

## <span data-ttu-id="268d3-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="268d3-152">RELATED LINKS</span></span>

[<span data-ttu-id="268d3-153">Add-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="268d3-153">Add-AzureRmServiceFabricClusterCertificate</span></span>](./Add-AzureRmServiceFabricClusterCertificate.md)

[<span data-ttu-id="268d3-154">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="268d3-154">New-AzureRmServiceFabricCluster</span></span>](./New-AzureRmServiceFabricCluster.md)
