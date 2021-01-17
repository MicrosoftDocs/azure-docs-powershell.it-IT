---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeUser.md
ms.openlocfilehash: 9074de6f4e6ee02a1476c1112d870b45d5bf6ccf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487664"
---
# <span data-ttu-id="707e7-101">Set-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="707e7-101">Set-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="707e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="707e7-102">SYNOPSIS</span></span>
<span data-ttu-id="707e7-103">Imposta una nuova password per un utente nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="707e7-103">Sets a new password for a user on the device.</span></span>

## <span data-ttu-id="707e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="707e7-104">SYNTAX</span></span>

### <span data-ttu-id="707e7-105">SetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="707e7-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="707e7-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="707e7-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -ResourceId <String> -Password <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="707e7-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="707e7-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeUser -InputObject <PSDataBoxEdgeUser> -Password <SecureString> -EncryptionKey <SecureString>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="707e7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="707e7-108">DESCRIPTION</span></span>
<span data-ttu-id="707e7-109">Il cmdlet **set-AzDataBoxEdgeUser** imposta una nuova password per un utente nel dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="707e7-109">The **Set-AzDataBoxEdgeUser** cmdlet sets a new password for a user on the Data Box Edge device.</span></span>

## <span data-ttu-id="707e7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="707e7-110">EXAMPLES</span></span>

### <span data-ttu-id="707e7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="707e7-111">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password @SecureString -EncryptionKey @SecureString
```

## <span data-ttu-id="707e7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="707e7-112">PARAMETERS</span></span>

### <span data-ttu-id="707e7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="707e7-113">-AsJob</span></span>
<span data-ttu-id="707e7-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="707e7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="707e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="707e7-115">-DefaultProfile</span></span>
<span data-ttu-id="707e7-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="707e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="707e7-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="707e7-117">-DeviceName</span></span>
<span data-ttu-id="707e7-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="707e7-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707e7-119">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="707e7-119">-EncryptionKey</span></span>
<span data-ttu-id="707e7-120">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="707e7-120">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="707e7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="707e7-121">-InputObject</span></span>
<span data-ttu-id="707e7-122">Oggetto di input</span><span class="sxs-lookup"><span data-stu-id="707e7-122">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707e7-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="707e7-123">-Name</span></span>
<span data-ttu-id="707e7-124">Username</span><span class="sxs-lookup"><span data-stu-id="707e7-124">Username</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707e7-125">-Password</span><span class="sxs-lookup"><span data-stu-id="707e7-125">-Password</span></span>
<span data-ttu-id="707e7-126">Password, specificare una stringa sicura</span><span class="sxs-lookup"><span data-stu-id="707e7-126">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="707e7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="707e7-127">-ResourceGroupName</span></span>
<span data-ttu-id="707e7-128">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="707e7-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707e7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="707e7-129">-ResourceId</span></span>
<span data-ttu-id="707e7-130">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="707e7-130">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="707e7-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="707e7-131">-Confirm</span></span>
<span data-ttu-id="707e7-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="707e7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="707e7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="707e7-133">-WhatIf</span></span>
<span data-ttu-id="707e7-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="707e7-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="707e7-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="707e7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="707e7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="707e7-136">CommonParameters</span></span>
<span data-ttu-id="707e7-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="707e7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="707e7-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="707e7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="707e7-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="707e7-139">INPUTS</span></span>

### <span data-ttu-id="707e7-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="707e7-140">None</span></span>

## <span data-ttu-id="707e7-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="707e7-141">OUTPUTS</span></span>

### <span data-ttu-id="707e7-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="707e7-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="707e7-143">Note</span><span class="sxs-lookup"><span data-stu-id="707e7-143">NOTES</span></span>

## <span data-ttu-id="707e7-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="707e7-144">RELATED LINKS</span></span>
