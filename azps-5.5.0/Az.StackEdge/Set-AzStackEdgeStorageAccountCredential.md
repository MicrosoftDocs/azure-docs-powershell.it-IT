---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 89e727b836f28ac1972bcf15e872e2860a8a6672
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176678"
---
# <span data-ttu-id="e24da-101">Set-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e24da-101">Set-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="e24da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e24da-102">SYNOPSIS</span></span>
<span data-ttu-id="e24da-103">Imposta le credenziali dell'account di archiviazione per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e24da-103">Sets the storage account credential for a device.</span></span>

## <span data-ttu-id="e24da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e24da-104">SYNTAX</span></span>

### <span data-ttu-id="e24da-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e24da-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e24da-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e24da-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -ResourceId <String> -StorageAccountAccessKey <SecureString>
 -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e24da-107">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e24da-107">SetByParentObjectParameterSet</span></span>
```
Set-AzStackEdgeStorageAccountCredential -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeStorageAccountCredential>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e24da-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e24da-108">DESCRIPTION</span></span>
<span data-ttu-id="e24da-109">Il cmdlet **Set-AzStackEdgeStorageAccountCredential** aggiorna le credenziali dell'account di archiviazione corrispondenti a un account di archiviazione nel dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="e24da-109">The **Set-AzStackEdgeStorageAccountCredential** cmdlet updates the storage account credential corresponding to a storage account on the Stack Edge device.</span></span>

## <span data-ttu-id="e24da-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e24da-110">EXAMPLES</span></span>

### <span data-ttu-id="e24da-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e24da-111">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAcountCredentialName
 -StorageAccountName storageaccountname -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                        StorageAccount      SslStatus  ResourceGroupName
--------------------------- ------------------- ---------- ---------------------
storageAcountCredentialName storageaccountname  Enabled    resourceGroupName
```

<span data-ttu-id="e24da-112">Informazioni sulla rotazione delle chiavi di accesso per un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e24da-112">Helps in rotating access keys for a storage account</span></span>

## <span data-ttu-id="e24da-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e24da-113">PARAMETERS</span></span>

### <span data-ttu-id="e24da-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e24da-114">-AsJob</span></span>
<span data-ttu-id="e24da-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e24da-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e24da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e24da-116">-DefaultProfile</span></span>
<span data-ttu-id="e24da-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e24da-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e24da-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e24da-118">-DeviceName</span></span>
<span data-ttu-id="e24da-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="e24da-119">Device Name</span></span>

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

### <span data-ttu-id="e24da-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e24da-120">-EncryptionKey</span></span>
<span data-ttu-id="e24da-121">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="e24da-121">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="e24da-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e24da-122">-InputObject</span></span>
<span data-ttu-id="e24da-123">Oggetto Input</span><span class="sxs-lookup"><span data-stu-id="e24da-123">Input Object</span></span>

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

### <span data-ttu-id="e24da-124">-Name</span><span class="sxs-lookup"><span data-stu-id="e24da-124">-Name</span></span>
<span data-ttu-id="e24da-125">Nome dell'account di archiviazione da usare</span><span class="sxs-lookup"><span data-stu-id="e24da-125">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="e24da-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e24da-126">-ResourceGroupName</span></span>
<span data-ttu-id="e24da-127">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e24da-127">Resource Group Name</span></span>

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

### <span data-ttu-id="e24da-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e24da-128">-ResourceId</span></span>
<span data-ttu-id="e24da-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e24da-129">Azure ResourceId</span></span>

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

### <span data-ttu-id="e24da-130">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="e24da-130">-StorageAccountAccessKey</span></span>
<span data-ttu-id="e24da-131">fornire la chiave di accesso dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e24da-131">provide storage account access key</span></span>

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

### <span data-ttu-id="e24da-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e24da-132">-Confirm</span></span>
<span data-ttu-id="e24da-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e24da-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e24da-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e24da-134">-WhatIf</span></span>
<span data-ttu-id="e24da-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e24da-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e24da-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e24da-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e24da-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e24da-137">CommonParameters</span></span>
<span data-ttu-id="e24da-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e24da-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e24da-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e24da-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e24da-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="e24da-140">INPUTS</span></span>

### <span data-ttu-id="e24da-141">System.String</span><span class="sxs-lookup"><span data-stu-id="e24da-141">System.String</span></span>

### <span data-ttu-id="e24da-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e24da-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="e24da-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e24da-143">OUTPUTS</span></span>

### <span data-ttu-id="e24da-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e24da-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="e24da-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="e24da-145">NOTES</span></span>

## <span data-ttu-id="e24da-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e24da-146">RELATED LINKS</span></span>
