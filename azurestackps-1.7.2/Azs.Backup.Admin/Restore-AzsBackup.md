---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35b937b810da65cc3cc2ed330198011ec108f9d6
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2020
ms.locfileid: "93865534"
---
# <span data-ttu-id="3c83b-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="3c83b-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="3c83b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c83b-102">SYNOPSIS</span></span>
<span data-ttu-id="3c83b-103">Ripristinare un backup.</span><span class="sxs-lookup"><span data-stu-id="3c83b-103">Restore a backup.</span></span>

## <span data-ttu-id="3c83b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c83b-104">SYNTAX</span></span>

### <span data-ttu-id="3c83b-105">Backups_Restore (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c83b-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>]
 -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c83b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c83b-106">ResourceId</span></span>
```
Restore-AzsBackup -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c83b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c83b-107">DESCRIPTION</span></span>
<span data-ttu-id="3c83b-108">Ripristinare un backup.</span><span class="sxs-lookup"><span data-stu-id="3c83b-108">Restore a backup.</span></span>

## <span data-ttu-id="3c83b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c83b-109">EXAMPLES</span></span>

### <span data-ttu-id="3c83b-110">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="3c83b-110">EXAMPLE 1</span></span>
```
Restore-AzsBackup -Name 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword
```

<span data-ttu-id="3c83b-111">Eseguire il ripristino da un backup di Azure stack.</span><span class="sxs-lookup"><span data-stu-id="3c83b-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="3c83b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c83b-112">PARAMETERS</span></span>

### <span data-ttu-id="3c83b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c83b-113">-AsJob</span></span>
<span data-ttu-id="3c83b-114">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="3c83b-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c83b-115">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="3c83b-115">-DecryptionCertPassword</span></span>
<span data-ttu-id="3c83b-116">Password del certificato di decrittazione.</span><span class="sxs-lookup"><span data-stu-id="3c83b-116">Password of the decryption cert.</span></span>

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

### <span data-ttu-id="3c83b-117">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="3c83b-117">-DecryptionCertPath</span></span>
<span data-ttu-id="3c83b-118">Percorso del file CERT di decrittografia con la chiave privata (PFX).</span><span class="sxs-lookup"><span data-stu-id="3c83b-118">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c83b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3c83b-119">-Force</span></span>
<span data-ttu-id="3c83b-120">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="3c83b-120">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c83b-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3c83b-121">-Location</span></span>
<span data-ttu-id="3c83b-122">Nome della posizione in cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="3c83b-122">Name of location to backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c83b-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c83b-123">-Name</span></span>
<span data-ttu-id="3c83b-124">Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="3c83b-124">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c83b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c83b-125">-ResourceGroupName</span></span>
<span data-ttu-id="3c83b-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3c83b-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c83b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c83b-127">-ResourceId</span></span>
<span data-ttu-id="3c83b-128">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="3c83b-128">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c83b-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3c83b-129">-Confirm</span></span>
<span data-ttu-id="3c83b-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c83b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c83b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c83b-131">-WhatIf</span></span>
<span data-ttu-id="3c83b-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c83b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c83b-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c83b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c83b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c83b-134">CommonParameters</span></span>
<span data-ttu-id="3c83b-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c83b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c83b-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c83b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c83b-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c83b-137">INPUTS</span></span>

## <span data-ttu-id="3c83b-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c83b-138">OUTPUTS</span></span>

## <span data-ttu-id="3c83b-139">Note</span><span class="sxs-lookup"><span data-stu-id="3c83b-139">NOTES</span></span>

## <span data-ttu-id="3c83b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c83b-140">RELATED LINKS</span></span>
