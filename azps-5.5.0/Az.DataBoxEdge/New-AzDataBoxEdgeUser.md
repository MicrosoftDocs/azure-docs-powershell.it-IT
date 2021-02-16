---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: a53f67c12a5c8d125319fc19f69db3ea9a57c5e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208786"
---
# <span data-ttu-id="6efb0-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="6efb0-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="6efb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6efb0-102">SYNOPSIS</span></span>
<span data-ttu-id="6efb0-103">Crea un nuovo utente per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6efb0-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="6efb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6efb0-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6efb0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6efb0-105">DESCRIPTION</span></span>
<span data-ttu-id="6efb0-106">Il cmdlet **New-AzDataBoxEdgeUser** crea un nuovo utente per il dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="6efb0-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="6efb0-107">È supportata la creazione solo di `Share` utenti di tipo.</span><span class="sxs-lookup"><span data-stu-id="6efb0-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="6efb0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6efb0-108">EXAMPLES</span></span>

### <span data-ttu-id="6efb0-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6efb0-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="6efb0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6efb0-110">PARAMETERS</span></span>

### <span data-ttu-id="6efb0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6efb0-111">-AsJob</span></span>
<span data-ttu-id="6efb0-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6efb0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6efb0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6efb0-113">-DefaultProfile</span></span>
<span data-ttu-id="6efb0-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6efb0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6efb0-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6efb0-115">-DeviceName</span></span>
<span data-ttu-id="6efb0-116">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="6efb0-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6efb0-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="6efb0-117">-EncryptionKey</span></span>
<span data-ttu-id="6efb0-118">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="6efb0-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="6efb0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6efb0-119">-Name</span></span>
<span data-ttu-id="6efb0-120">Nome utente</span><span class="sxs-lookup"><span data-stu-id="6efb0-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6efb0-121">-Password</span><span class="sxs-lookup"><span data-stu-id="6efb0-121">-Password</span></span>
<span data-ttu-id="6efb0-122">Password, fornisci come stringa sicura</span><span class="sxs-lookup"><span data-stu-id="6efb0-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="6efb0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6efb0-123">-ResourceGroupName</span></span>
<span data-ttu-id="6efb0-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6efb0-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6efb0-125">-Type</span><span class="sxs-lookup"><span data-stu-id="6efb0-125">-Type</span></span>
<span data-ttu-id="6efb0-126">Selezionare UserType</span><span class="sxs-lookup"><span data-stu-id="6efb0-126">Select UserType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6efb0-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6efb0-127">-Confirm</span></span>
<span data-ttu-id="6efb0-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6efb0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6efb0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6efb0-129">-WhatIf</span></span>
<span data-ttu-id="6efb0-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6efb0-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6efb0-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6efb0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6efb0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6efb0-132">CommonParameters</span></span>
<span data-ttu-id="6efb0-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6efb0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6efb0-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6efb0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6efb0-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="6efb0-135">INPUTS</span></span>

### <span data-ttu-id="6efb0-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6efb0-136">None</span></span>

## <span data-ttu-id="6efb0-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6efb0-137">OUTPUTS</span></span>

### <span data-ttu-id="6efb0-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="6efb0-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="6efb0-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="6efb0-139">NOTES</span></span>

## <span data-ttu-id="6efb0-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6efb0-140">RELATED LINKS</span></span>
