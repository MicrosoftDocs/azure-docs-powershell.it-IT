---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 89e727b836f28ac1972bcf15e872e2860a8a6672
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473673"
---
# <span data-ttu-id="3fbef-101">Set-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3fbef-101">Set-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="3fbef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3fbef-102">SYNOPSIS</span></span>
<span data-ttu-id="3fbef-103">Imposta le credenziali dell'account di archiviazione per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3fbef-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="3fbef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3fbef-104">SYNTAX</span></span>

### <span data-ttu-id="3fbef-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3fbef-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fbef-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fbef-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3fbef-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fbef-107">SetByParentObjectParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fbef-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fbef-108">DESCRIPTION</span></span>
<span data-ttu-id="3fbef-109">Il cmdlet **set-AzStackEdgeStorageAccountCredential** aggiorna le credenziali dell'account di archiviazione corrispondenti a un account di archiviazione nel dispositivo dello stack Edge.</span><span class="sxs-lookup"><span data-stu-id="3fbef-109">The **Set-AzStackEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Stack Edge device.</span></span>

## <span data-ttu-id="3fbef-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3fbef-110">EXAMPLES</span></span>

### <span data-ttu-id="3fbef-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3fbef-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="3fbef-112">Consente di ruotare i tasti di scelta per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3fbef-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="3fbef-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3fbef-113">PARAMETERS</span></span>

### <span data-ttu-id="3fbef-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fbef-114">-AsJob</span></span>
<span data-ttu-id="3fbef-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3fbef-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3fbef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fbef-116">-DefaultProfile</span></span>
<span data-ttu-id="3fbef-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3fbef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fbef-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3fbef-118">-DeviceName</span></span>
<span data-ttu-id="3fbef-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="3fbef-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbef-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="3fbef-120">-EncryptionKey</span></span>
<span data-ttu-id="3fbef-121">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="3fbef-121">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fbef-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fbef-122">-InputObject</span></span>
<span data-ttu-id="3fbef-123">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="3fbef-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: SetByParentObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbef-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="3fbef-124">-Name</span></span>
<span data-ttu-id="3fbef-125">Nome dell'account di archiviazione da usare</span><span class="sxs-lookup"><span data-stu-id="3fbef-125">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fbef-126">-ResourceGroupName</span></span>
<span data-ttu-id="3fbef-127">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="3fbef-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbef-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fbef-128">-ResourceId</span></span>
<span data-ttu-id="3fbef-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fbef-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fbef-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="3fbef-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="3fbef-131">Immettere il codice di accesso dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3fbef-131">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fbef-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3fbef-132">-Confirm</span></span>
<span data-ttu-id="3fbef-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fbef-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fbef-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fbef-134">-WhatIf</span></span>
<span data-ttu-id="3fbef-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3fbef-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3fbef-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3fbef-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fbef-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fbef-137">CommonParameters</span></span>
<span data-ttu-id="3fbef-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fbef-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fbef-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3fbef-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fbef-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3fbef-140">INPUTS</span></span>

### <span data-ttu-id="3fbef-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3fbef-141">System.String</span></span>

### <span data-ttu-id="3fbef-142">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3fbef-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="3fbef-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3fbef-143">OUTPUTS</span></span>

### <span data-ttu-id="3fbef-144">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3fbef-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="3fbef-145">Note</span><span class="sxs-lookup"><span data-stu-id="3fbef-145">NOTES</span></span>

## <span data-ttu-id="3fbef-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3fbef-146">RELATED LINKS</span></span>
