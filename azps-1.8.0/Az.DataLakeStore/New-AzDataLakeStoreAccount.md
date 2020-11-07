---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
ms.openlocfilehash: 64af4b5d8bf159332c757982fcd1b2f7e949f3ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684525"
---
# <span data-ttu-id="323c5-101">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="323c5-101">New-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="323c5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="323c5-102">SYNOPSIS</span></span>
<span data-ttu-id="323c5-103">Crea un nuovo account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="323c5-103">Creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="323c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="323c5-104">SYNTAX</span></span>

### <span data-ttu-id="323c5-105">UserOrSystemAssignedEncryption (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="323c5-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="323c5-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="323c5-106">DisableEncryption</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="323c5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="323c5-107">DESCRIPTION</span></span>
<span data-ttu-id="323c5-108">Il cmdlet **New-AzDataLakeStoreAccount** crea un nuovo account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="323c5-108">The **New-AzDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="323c5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="323c5-109">EXAMPLES</span></span>

### <span data-ttu-id="323c5-110">Esempio 1: creare un account</span><span class="sxs-lookup"><span data-stu-id="323c5-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="323c5-111">Questo comando crea un account di data Lake Store denominato ContosoADL per la posizione est degli Stati Uniti 2.</span><span class="sxs-lookup"><span data-stu-id="323c5-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="323c5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="323c5-112">PARAMETERS</span></span>

### <span data-ttu-id="323c5-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="323c5-113">-DefaultGroup</span></span>
<span data-ttu-id="323c5-114">Specifica l'ID oggetto del gruppo di directory AzureActive da usare come proprietario del gruppo predefinito per nuovi file e cartelle.</span><span class="sxs-lookup"><span data-stu-id="323c5-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="323c5-115">-DefaultProfile</span></span>
<span data-ttu-id="323c5-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="323c5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="323c5-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="323c5-117">-DisableEncryption</span></span>
<span data-ttu-id="323c5-118">Indica che all'account non verrà applicata alcuna forma di crittografia.</span><span class="sxs-lookup"><span data-stu-id="323c5-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEncryption
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323c5-119">-Crittografia</span><span class="sxs-lookup"><span data-stu-id="323c5-119">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323c5-120">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="323c5-120">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323c5-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="323c5-121">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323c5-122">-Versione</span><span class="sxs-lookup"><span data-stu-id="323c5-122">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323c5-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="323c5-123">-Location</span></span>
<span data-ttu-id="323c5-124">Specifica la posizione da usare per l'account.</span><span class="sxs-lookup"><span data-stu-id="323c5-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="323c5-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="323c5-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="323c5-126">Stati Uniti Est 2</span><span class="sxs-lookup"><span data-stu-id="323c5-126">East US 2</span></span>

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

### <span data-ttu-id="323c5-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="323c5-127">-Name</span></span>
<span data-ttu-id="323c5-128">Specifica il nome dell'account da creare.</span><span class="sxs-lookup"><span data-stu-id="323c5-128">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="323c5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="323c5-129">-ResourceGroupName</span></span>
<span data-ttu-id="323c5-130">Specifica il nome del gruppo di risorse che contiene l'account.</span><span class="sxs-lookup"><span data-stu-id="323c5-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="323c5-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="323c5-131">-Tag</span></span>
<span data-ttu-id="323c5-132">Specifica i tag come coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="323c5-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="323c5-133">Puoi usare i tag per identificare un account di data Lake Store da altre risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="323c5-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323c5-134">-Tier</span><span class="sxs-lookup"><span data-stu-id="323c5-134">-Tier</span></span>
<span data-ttu-id="323c5-135">Il livello di impegno desiderato per l'account da usare.</span><span class="sxs-lookup"><span data-stu-id="323c5-135">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="323c5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="323c5-136">CommonParameters</span></span>
<span data-ttu-id="323c5-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="323c5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="323c5-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="323c5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="323c5-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="323c5-139">INPUTS</span></span>

### <span data-ttu-id="323c5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="323c5-140">System.String</span></span>

### <span data-ttu-id="323c5-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="323c5-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="323c5-142">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. EncryptionConfigType, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="323c5-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="323c5-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="323c5-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="323c5-144">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. TierType, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="323c5-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="323c5-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="323c5-145">OUTPUTS</span></span>

### <span data-ttu-id="323c5-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="323c5-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="323c5-147">Note</span><span class="sxs-lookup"><span data-stu-id="323c5-147">NOTES</span></span>

## <span data-ttu-id="323c5-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="323c5-148">RELATED LINKS</span></span>

[<span data-ttu-id="323c5-149">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="323c5-149">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="323c5-150">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="323c5-150">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="323c5-151">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="323c5-151">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="323c5-152">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="323c5-152">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


