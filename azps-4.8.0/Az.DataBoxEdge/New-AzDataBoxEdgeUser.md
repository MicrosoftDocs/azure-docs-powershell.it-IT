---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: a53f67c12a5c8d125319fc19f69db3ea9a57c5e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190807"
---
# <span data-ttu-id="8dd88-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="8dd88-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="8dd88-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8dd88-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd88-103">Crea un nuovo utente per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8dd88-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="8dd88-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8dd88-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dd88-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8dd88-105">DESCRIPTION</span></span>
<span data-ttu-id="8dd88-106">Il cmdlet **New-AzDataBoxEdgeUser** crea un nuovo utente per il dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="8dd88-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="8dd88-107">È supportata la creazione di solo utenti di tipo `Share` .</span><span class="sxs-lookup"><span data-stu-id="8dd88-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="8dd88-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8dd88-108">EXAMPLES</span></span>

### <span data-ttu-id="8dd88-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8dd88-109">Example 1</span></span>
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

## <span data-ttu-id="8dd88-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8dd88-110">PARAMETERS</span></span>

### <span data-ttu-id="8dd88-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8dd88-111">-AsJob</span></span>
<span data-ttu-id="8dd88-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8dd88-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8dd88-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd88-113">-DefaultProfile</span></span>
<span data-ttu-id="8dd88-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd88-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dd88-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8dd88-115">-DeviceName</span></span>
<span data-ttu-id="8dd88-116">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="8dd88-116">Device Name</span></span>

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

### <span data-ttu-id="8dd88-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="8dd88-117">-EncryptionKey</span></span>
<span data-ttu-id="8dd88-118">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="8dd88-118">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="8dd88-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8dd88-119">-Name</span></span>
<span data-ttu-id="8dd88-120">Username</span><span class="sxs-lookup"><span data-stu-id="8dd88-120">Username</span></span>

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

### <span data-ttu-id="8dd88-121">-Password</span><span class="sxs-lookup"><span data-stu-id="8dd88-121">-Password</span></span>
<span data-ttu-id="8dd88-122">Password, specificare una stringa sicura</span><span class="sxs-lookup"><span data-stu-id="8dd88-122">Password, provide as a secure string</span></span>

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

### <span data-ttu-id="8dd88-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd88-123">-ResourceGroupName</span></span>
<span data-ttu-id="8dd88-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="8dd88-124">Resource Group Name</span></span>

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

### <span data-ttu-id="8dd88-125">-Digitare</span><span class="sxs-lookup"><span data-stu-id="8dd88-125">-Type</span></span>
<span data-ttu-id="8dd88-126">Selezionare UserType</span><span class="sxs-lookup"><span data-stu-id="8dd88-126">Select UserType</span></span>

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

### <span data-ttu-id="8dd88-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8dd88-127">-Confirm</span></span>
<span data-ttu-id="8dd88-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dd88-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dd88-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dd88-129">-WhatIf</span></span>
<span data-ttu-id="8dd88-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8dd88-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dd88-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8dd88-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dd88-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd88-132">CommonParameters</span></span>
<span data-ttu-id="8dd88-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dd88-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd88-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dd88-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd88-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8dd88-135">INPUTS</span></span>

### <span data-ttu-id="8dd88-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8dd88-136">None</span></span>

## <span data-ttu-id="8dd88-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8dd88-137">OUTPUTS</span></span>

### <span data-ttu-id="8dd88-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8dd88-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="8dd88-139">Note</span><span class="sxs-lookup"><span data-stu-id="8dd88-139">NOTES</span></span>

## <span data-ttu-id="8dd88-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8dd88-140">RELATED LINKS</span></span>
