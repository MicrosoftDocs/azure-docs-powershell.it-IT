---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7642F18A-B193-4849-BE3C-1B85FBD213F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverbackuplongtermretentionvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerBackupLongTermRetentionVault.md
ms.openlocfilehash: 0abdfdb78c8564afd4cac2661c4f390f5831b73f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687403"
---
# <span data-ttu-id="c5e90-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="c5e90-101">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>

## <span data-ttu-id="c5e90-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c5e90-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e90-103">Imposta un Vault di conservazione a lungo termine del server.</span><span class="sxs-lookup"><span data-stu-id="c5e90-103">Sets a server long term retention vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5e90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5e90-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerBackupLongTermRetentionVault -ResourceId <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5e90-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5e90-105">DESCRIPTION</span></span>
<span data-ttu-id="c5e90-106">Il cmdlet **set-AzureRmSqlServerBackupLongTermRetentionVault** imposta il Vault di conservazione a lungo termine registrato nel server.</span><span class="sxs-lookup"><span data-stu-id="c5e90-106">The **Set-AzureRmSqlServerBackupLongTermRetentionVault** cmdlet sets the long term retention vault registered to this server.</span></span>
<span data-ttu-id="c5e90-107">Il Vault è una risorsa di backup di Azure usata per archiviare i dati di backup.</span><span class="sxs-lookup"><span data-stu-id="c5e90-107">The vault is an Azure Backup resource used to store backup data.</span></span>

## <span data-ttu-id="c5e90-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5e90-108">EXAMPLES</span></span>

## <span data-ttu-id="c5e90-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c5e90-109">PARAMETERS</span></span>

### <span data-ttu-id="c5e90-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e90-110">-DefaultProfile</span></span>
<span data-ttu-id="c5e90-111">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c5e90-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e90-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5e90-112">-ResourceGroupName</span></span>
<span data-ttu-id="c5e90-113">Specifica il nome del gruppo di risorse che contiene il server.</span><span class="sxs-lookup"><span data-stu-id="c5e90-113">Specifies the name of the resource group that contains the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e90-114">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5e90-114">-ResourceId</span></span>
<span data-ttu-id="c5e90-115">Specifica l'ID di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="c5e90-115">Specifies the ID of a resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e90-116">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="c5e90-116">-ServerName</span></span>
<span data-ttu-id="c5e90-117">Specifica il server per cui questo cmdlet imposta un Vault.</span><span class="sxs-lookup"><span data-stu-id="c5e90-117">Specifies the server for which this cmdlet sets a vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5e90-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c5e90-118">-Confirm</span></span>
<span data-ttu-id="c5e90-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5e90-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e90-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5e90-120">-WhatIf</span></span>
<span data-ttu-id="c5e90-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5e90-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5e90-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5e90-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e90-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e90-123">CommonParameters</span></span>
<span data-ttu-id="c5e90-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5e90-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e90-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5e90-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e90-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c5e90-126">INPUTS</span></span>

### <span data-ttu-id="c5e90-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c5e90-127">None</span></span>
<span data-ttu-id="c5e90-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c5e90-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c5e90-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5e90-129">OUTPUTS</span></span>

## <span data-ttu-id="c5e90-130">Note</span><span class="sxs-lookup"><span data-stu-id="c5e90-130">NOTES</span></span>

## <span data-ttu-id="c5e90-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5e90-131">RELATED LINKS</span></span>

[<span data-ttu-id="c5e90-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="c5e90-132">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>](./Get-AzureRmSqlServerBackupLongTermRetentionVault.md)

[<span data-ttu-id="c5e90-133">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="c5e90-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)