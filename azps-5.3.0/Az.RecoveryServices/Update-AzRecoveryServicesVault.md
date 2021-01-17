---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
ms.openlocfilehash: cdde8169c4b068b986910dc3bfc5de446833f5ff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378290"
---
# <span data-ttu-id="2bf80-101">Update-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="2bf80-101">Update-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="2bf80-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2bf80-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf80-103">Aggiorna MSI nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="2bf80-103">Updates MSI to the recovery services vault.</span></span>

## <span data-ttu-id="2bf80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2bf80-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesVault -ResourceGroupName <string> -Name <string> -IdentityType <MSIdentity>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bf80-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bf80-105">DESCRIPTION</span></span>
<span data-ttu-id="2bf80-106">Questo cmdlet viene usato per aggiungere o rimuovere il file MSI dall'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="2bf80-106">This cmdlet is used to add or remove  the MSI from the recovery services vault.</span></span> <span data-ttu-id="2bf80-107">USA-IdentityType param per assegnare un'identità SystemAssigned a RSVault.</span><span class="sxs-lookup"><span data-stu-id="2bf80-107">Use -IdentityType param to assign a SystemAssigned identity to the RSVault.</span></span> <span data-ttu-id="2bf80-108">USA IdentityType None per rimuovere il file MSI dalla volta.</span><span class="sxs-lookup"><span data-stu-id="2bf80-108">Use IdentityType None to remove the MSI from the vault.</span></span>

## <span data-ttu-id="2bf80-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2bf80-109">EXAMPLES</span></span>

### <span data-ttu-id="2bf80-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2bf80-110">Example 1</span></span>
```powershell
PS C:\> Update-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName" -IdentityType SystemAssigned
```

<span data-ttu-id="2bf80-111">Questo cmdlet viene usato per aggiungere un'identità SystemAssigned a un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="2bf80-111">This cmdlet is used to add a SystemAssigned identity to a recovery services vault.</span></span>

## <span data-ttu-id="2bf80-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2bf80-112">PARAMETERS</span></span>

### <span data-ttu-id="2bf80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf80-113">-DefaultProfile</span></span>
<span data-ttu-id="2bf80-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2bf80-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf80-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2bf80-115">-Name</span></span>

<span data-ttu-id="2bf80-116">Specifica il nome del Vault di servizi di ripristino da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="2bf80-116">Specifies the name of the recovery services vault to update.</span></span>

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

### <span data-ttu-id="2bf80-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bf80-117">-ResourceGroupName</span></span>

<span data-ttu-id="2bf80-118">Specifica il nome del gruppo di risorse Azure in cui è presente il Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="2bf80-118">Specifies the name of the Azure resource group where recovery services vault is present.</span></span>

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

### <span data-ttu-id="2bf80-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2bf80-119">-IdentityType</span></span>
<span data-ttu-id="2bf80-120">Il tipo MSI assegnato a servizio ripristino servizi di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2bf80-120">The MSI type assigned to Recovery Services Vault.</span></span>

```yaml
Type: MSIdentity
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf80-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2bf80-121">-Confirm</span></span>
<span data-ttu-id="2bf80-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bf80-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf80-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bf80-123">-WhatIf</span></span>
<span data-ttu-id="2bf80-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2bf80-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bf80-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2bf80-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bf80-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf80-126">CommonParameters</span></span>
<span data-ttu-id="2bf80-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bf80-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf80-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2bf80-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf80-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2bf80-129">INPUTS</span></span>

### <span data-ttu-id="2bf80-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2bf80-130">System.String</span></span>

## <span data-ttu-id="2bf80-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2bf80-131">OUTPUTS</span></span>

### <span data-ttu-id="2bf80-132">Microsoft. Azure. Management. RecoveryServices. Models. Vault</span><span class="sxs-lookup"><span data-stu-id="2bf80-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span></span>

## <span data-ttu-id="2bf80-133">Note</span><span class="sxs-lookup"><span data-stu-id="2bf80-133">NOTES</span></span>

## <span data-ttu-id="2bf80-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2bf80-134">RELATED LINKS</span></span>
