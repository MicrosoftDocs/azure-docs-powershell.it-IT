---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0EB5C25C-D0A1-4444-AEA2-C963D5069CFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreAccount.md
ms.openlocfilehash: 15a99d07630f6060473f66f985cfa8b8bf06d1e4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189077"
---
# <span data-ttu-id="66b52-101">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="66b52-101">Set-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="66b52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66b52-102">SYNOPSIS</span></span>
<span data-ttu-id="66b52-103">Modifica un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="66b52-103">Modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="66b52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66b52-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreAccount [-Name] <String> [[-DefaultGroup] <String>] [[-Tag] <Hashtable>]
 [[-TrustedIdProviderState] <TrustedIdProviderState>] [[-FirewallState] <FirewallState>]
 [[-ResourceGroupName] <String>] [-Tier <TierType>] [-AllowAzureIpState <FirewallAllowAzureIpsState>]
 [-KeyVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66b52-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66b52-105">DESCRIPTION</span></span>
<span data-ttu-id="66b52-106">Il cmdlet **set-AzDataLakeStoreAccount** modifica un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="66b52-106">The **Set-AzDataLakeStoreAccount** cmdlet modifies a Data Lake Store account.</span></span>

## <span data-ttu-id="66b52-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66b52-107">EXAMPLES</span></span>

### <span data-ttu-id="66b52-108">Esempio 1: aggiungere un contrassegno a un account</span><span class="sxs-lookup"><span data-stu-id="66b52-108">Example 1: Add a tag to an account</span></span>
```powershell
PS C:\>Set-AzDataLakeStoreAccount -Name "ContosoADL" -Tags @{"stage"="production"}
```

<span data-ttu-id="66b52-109">Questo comando aggiunge il tag specificato all'account di data Lake Store denominato ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="66b52-109">This command adds the specified tag to the Data Lake Store account named ContosoADL.</span></span>

### <span data-ttu-id="66b52-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="66b52-110">Example 2</span></span>

<span data-ttu-id="66b52-111">Modifica un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="66b52-111">Modifies a Data Lake Store account.</span></span> <span data-ttu-id="66b52-112">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="66b52-112">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Set-AzDataLakeStoreAccount -FirewallState Enabled -Name 'ContosoADL'
```

## <span data-ttu-id="66b52-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66b52-113">PARAMETERS</span></span>

### <span data-ttu-id="66b52-114">-AllowAzureIpState</span><span class="sxs-lookup"><span data-stu-id="66b52-114">-AllowAzureIpState</span></span>
<span data-ttu-id="66b52-115">Facoltativamente Consenti/blocca l'IPs originario di Azure attraverso il firewall.</span><span class="sxs-lookup"><span data-stu-id="66b52-115">Optionally allow/block Azure originating IPs through the firewall.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66b52-116">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="66b52-116">-DefaultGroup</span></span>
<span data-ttu-id="66b52-117">Specifica l'ID di un gruppo di directory AzureActive.</span><span class="sxs-lookup"><span data-stu-id="66b52-117">Specifies the ID of an AzureActive Directory group.</span></span>
<span data-ttu-id="66b52-118">Questo gruppo è il gruppo predefinito per i file e le cartelle creati.</span><span class="sxs-lookup"><span data-stu-id="66b52-118">This group is the default group for files and folders that you create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66b52-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66b52-119">-DefaultProfile</span></span>
<span data-ttu-id="66b52-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="66b52-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66b52-121">-FirewallState</span><span class="sxs-lookup"><span data-stu-id="66b52-121">-FirewallState</span></span>
<span data-ttu-id="66b52-122">Facoltativamente abilitare o disabilitare le regole del firewall esistenti.</span><span class="sxs-lookup"><span data-stu-id="66b52-122">Optionally enable or disable existing firewall rules.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState]
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66b52-123">-Versione</span><span class="sxs-lookup"><span data-stu-id="66b52-123">-KeyVersion</span></span>
<span data-ttu-id="66b52-124">Se il tipo di crittografia è assegnato dall'utente, l'utente può ruotare la propria versione chiave con questo parametro.</span><span class="sxs-lookup"><span data-stu-id="66b52-124">If the encryption type is User assigned, the user can rotate their key version with this parameter.</span></span>

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

### <span data-ttu-id="66b52-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="66b52-125">-Name</span></span>
<span data-ttu-id="66b52-126">Specifica il nome di un account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="66b52-126">Specifies the name of a Data Lake Store account.</span></span>

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

### <span data-ttu-id="66b52-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66b52-127">-ResourceGroupName</span></span>
<span data-ttu-id="66b52-128">Specifica il nome del gruppo di risorse che contiene l'account di data Lake Store da modificare.</span><span class="sxs-lookup"><span data-stu-id="66b52-128">Specifies the name of the resource group that contains the Data Lake Store account to modify.</span></span>

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

### <span data-ttu-id="66b52-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="66b52-129">-Tag</span></span>
<span data-ttu-id="66b52-130">Specifica i tag come coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="66b52-130">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="66b52-131">Puoi usare i tag per identificare un account di data Lake Store da altre risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="66b52-131">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66b52-132">-Tier</span><span class="sxs-lookup"><span data-stu-id="66b52-132">-Tier</span></span>
<span data-ttu-id="66b52-133">Il livello di impegno desiderato per l'account da usare.</span><span class="sxs-lookup"><span data-stu-id="66b52-133">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="66b52-134">-TrustedIdProviderState</span><span class="sxs-lookup"><span data-stu-id="66b52-134">-TrustedIdProviderState</span></span>
<span data-ttu-id="66b52-135">Abilitare o disabilitare facoltativamente i provider di ID attendibili esistenti.</span><span class="sxs-lookup"><span data-stu-id="66b52-135">Optionally enable or disable the existing trusted ID providers.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66b52-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b52-136">CommonParameters</span></span>
<span data-ttu-id="66b52-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66b52-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b52-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66b52-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b52-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66b52-139">INPUTS</span></span>

### <span data-ttu-id="66b52-140">System. String</span><span class="sxs-lookup"><span data-stu-id="66b52-140">System.String</span></span>

### <span data-ttu-id="66b52-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="66b52-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="66b52-142">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. TrustedIdProviderState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="66b52-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TrustedIdProviderState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="66b52-143">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. FirewallState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="66b52-143">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="66b52-144">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. TierType, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="66b52-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="66b52-145">System. Nullable ' 1 [[Microsoft. Azure. Management. datalake. Store. Models. FirewallAllowAzureIpsState, Microsoft. Azure. Management. datalake. Store, Version = 2.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="66b52-145">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.FirewallAllowAzureIpsState, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="66b52-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66b52-146">OUTPUTS</span></span>

### <span data-ttu-id="66b52-147">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="66b52-147">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="66b52-148">Note</span><span class="sxs-lookup"><span data-stu-id="66b52-148">NOTES</span></span>

## <span data-ttu-id="66b52-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66b52-149">RELATED LINKS</span></span>

[<span data-ttu-id="66b52-150">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="66b52-150">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="66b52-151">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="66b52-151">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="66b52-152">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="66b52-152">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="66b52-153">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="66b52-153">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)

