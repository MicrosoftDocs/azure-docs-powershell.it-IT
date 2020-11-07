---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7642F18A-B193-4849-BE3C-1B85FBD213F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 663ac3d8342e5ba231276e560408f8f7f6e74741
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688500"
---
# <span data-ttu-id="11b9e-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="11b9e-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="11b9e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11b9e-102">SYNOPSIS</span></span>
<span data-ttu-id="11b9e-103">Imposta un Vault di conservazione a lungo termine del server.</span><span class="sxs-lookup"><span data-stu-id="11b9e-103">Sets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11b9e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11b9e-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerBackupLongTermRetentionVault -ResourceId <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11b9e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11b9e-105">DESCRIPTION</span></span>
<span data-ttu-id="11b9e-106">Il cmdlet **set-AzureRmSqlServerBackupLongTermRetentionVault** imposta il Vault di conservazione a lungo termine registrato nel server.</span><span class="sxs-lookup"><span data-stu-id="11b9e-106">The **Set-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet sets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="11b9e-107">Il Vault è una risorsa di backup di Azure usata per archiviare i dati di backup.</span><span class="sxs-lookup"><span data-stu-id="11b9e-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="11b9e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11b9e-108">EXAMPLES</span></span>

## <span data-ttu-id="11b9e-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11b9e-109">PARAMETERS</span></span>

### <span data-ttu-id="11b9e-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11b9e-110">-ResourceGroupName</span></span>
<span data-ttu-id="11b9e-111">Specifica il nome del gruppo di risorse che contiene il server.</span><span class="sxs-lookup"><span data-stu-id="11b9e-111">Specifies the name of the resource group that contains the server.</span></span>

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

### <span data-ttu-id="11b9e-112">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11b9e-112">-ResourceId</span></span>
<span data-ttu-id="11b9e-113">Specifica l'ID di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="11b9e-113">Specifies the ID of a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11b9e-114">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="11b9e-114">-ServerName</span></span>
<span data-ttu-id="11b9e-115">Specifica il server per cui questo cmdlet imposta un Vault.</span><span class="sxs-lookup"><span data-stu-id="11b9e-115">Specifies the server for which this cmdlet sets a vault.</span></span>

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

### <span data-ttu-id="11b9e-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="11b9e-116">-Confirm</span></span>
<span data-ttu-id="11b9e-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11b9e-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b9e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11b9e-118">-WhatIf</span></span>
<span data-ttu-id="11b9e-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11b9e-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11b9e-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11b9e-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b9e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b9e-121">-DefaultProfile</span></span>
<span data-ttu-id="11b9e-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11b9e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11b9e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b9e-123">CommonParameters</span></span>
<span data-ttu-id="11b9e-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11b9e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b9e-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11b9e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b9e-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11b9e-126">INPUTS</span></span>

## <span data-ttu-id="11b9e-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11b9e-127">OUTPUTS</span></span>

## <span data-ttu-id="11b9e-128">Note</span><span class="sxs-lookup"><span data-stu-id="11b9e-128">NOTES</span></span>

## <span data-ttu-id="11b9e-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11b9e-129">RELATED LINKS</span></span>

[<span data-ttu-id="11b9e-130">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="11b9e-130">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Get-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="11b9e-131">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="11b9e-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
